<template>
    <div id="contact">
        <h2>Get in Touch</h2>
        <div id="contact-form">
            <form method="POST" action="https://formspree.io/pabloleonpsico@gmail.com">
                <input type="hidden" name="_subject" value="Contact request from personal website" />
                <input type="email" name="_replyto" placeholder="Your email" required>
                <textarea name="message" placeholder="Your message" required></textarea>
                <button type="submit">Send</button>
            </form>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Contact'
}
</script>
<style lang="scss" scoped>

$secondary-color: #91842f;

@mixin transition($duration: 0.5s, $func: ease, $property: all) {
    transition: #{$duration} #{$func} #{$property};
}

@mixin placeholder {
    &::-webkit-input-placeholder {
        @content;
    }

    &:-moz-placeholder {
        @content;
        opacity: 1;
    }

    &::-moz-placeholder {
        @content;
        opacity: 1;
    }

    &:-ms-input-placeholder {
        @content;
    }
}

#contact {
    background: linear-gradient(to bottom, $secondary-color 0%, white 2%);

    padding: 50px 15px;
    text-align: center;
    h2 {
        margin: 0 0 15px 0;
        color: $secondary-color;
        font-weight: 500;
    }
}

#contact-form {
    max-width: 500px;
    margin: 0 auto;
    form{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    input, textarea {
        display: block;
        width: 100%;
     
        padding: 10px;
        border-radius: 4px;
        border: none;
        margin-bottom: 10px;
        background: $secondary-color;
        color: #fff;
        @include transition();
        @include placeholder {
            color: #fff;
        }

        &:focus {
            outline: none;
            background: darken($secondary-color, 5%);
        }
    }

    textarea {
        height: 150px;
        resize: none;
    }

    button[type="submit"] {
        display: block;
        width: 100%;
        background: #fff;
        border-radius: 4px;
        padding: 5px 10px;
        border: none;
        color: $secondary-color;
        font-weight: 700;
        box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
        @include transition();

        &:hover {
            box-shadow: 0 8px 15px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
        }
    }
}
</style>