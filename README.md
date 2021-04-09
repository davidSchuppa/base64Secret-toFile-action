# base64Secret-toFile-action

This Github action helps reading a base64 encoded file, decode it and puts it on the defined path. If the directory doesn't exists, it creates it.

Simple example
```yaml
steps:
  - name: Action 1
    uses: ...

  - name: Action 2
    run: ...

  - name: Decode secret
    uses: davidSchuppa/base64Secret-toFile-action@v1
    with:
        secret: ${{ secrets.MY_AWESOME_SECRET_KEY }}
        filename: myFile.txt
        destination-path: ~/dirForMyFile
```