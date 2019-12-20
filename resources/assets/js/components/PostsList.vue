<template>
    <section class="posts container">

        <!-- @if (isset($title))
            <h3>{{ $title }}</h3>
        @endif -->

        <posts-list-item
            v-for="post in items"
            :post="post"
            :key="post.id"
        />

        <!-- @empty -->
        <article class="post" v-if="! items.length">
            <div class="content-post">
                <h1>No hay publicaciones todavía.</h1>
            </div>
        </article>
        <!-- @endforelse -->
    </section><!-- fin del section.posts -->
    <!-- {{ $posts->appends(request()->all())->links() }} -->
</template>

<script>
    export default {
        props: ['items']
    }
</script>
