# Features

There are a lot of features to easily manage your database server.

## List servers

You can get a list of all servers linked to your app by running:

```
vapor cloud database list
```

## Tail logs

!!! warning
    This feature is not implemented yet.

To tail the database logs, you can run:

```
vapor cloud database logs --token=<TOKEN>
```

It will default to past `5 minutes`. To get more history, you can pass `--since` e.g.:

```
vapor cloud database logs --token=<TOKEN> --since=20m

vapor cloud database logs --token=<TOKEN> --since=2h
```

## Restart server

If you ever need to restart your database server, you can easily run the restart command:

```
vapor cloud database restart --token=<TOKEN>
```

## Shutdown server

If you don't need the database server in some time, but still want the data, and would be able to spin it up fast, you can shut it down.

```
vapor cloud database shutdown --token=<TOKEN>
```

## Delete server

If you don't need your database server again, you can delete the server. After 24 hours the data will be wiped, and can't be reconstructed, make sure to take a local backup before.

```
vapor cloud database delete --token=<TOKEN>
```