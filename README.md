Router for React.

Use @Mixin on the client and @create on the server.

On the client, @Mixin goes into the root component and sets
route matches into props.matchedRoute.

Expects a path list:

    routes =  [
        { path: "/",                 handler: Home },
        { path: "/writing",          handler: Writing },
        { path: "/writing/:slug",    handler: WritingView },
        { path: "*",                 handler: NotFound }
    ]

When matchRoute(path) is called, a matchedRoute object
is set into this.props:

    matchedRoute:
        path: "/writing/my-post"
        params:
            slug: "my-post"
        handler: WritingView

