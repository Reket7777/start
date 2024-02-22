<!-- HTML блок коду -->
<div style="width: 200px; height: 200px;">
    <!-- Внутрішні блоки для створення куба -->
    <div class="cube">
        <div class="face front">Front</div>
        <div class="face back">Back</div>
        <div class="face left">Left</div>
        <div class="face right">Right</div>
        <div class="face top">Top</div>
        <div class="face bottom">Bottom</div>
    </div>
</div>

<!-- CSS стилі -->
<style>
    .cube {
        width: 100%;
        height: 100%;
        position: relative;
        transform-style: preserve-3d;
        animation: spin 5s infinite linear;
    }

    .face {
        width: 100%;
        height: 100%;
        position: absolute;
        background: #f00;
        opacity: 0.7;
    }

    .front {
        transform: rotateY(0deg) translateZ(50px);
    }

    .back {
        transform: rotateY(180deg) translateZ(50px);
    }

    .left {
        transform: rotateY(-90deg) translateZ(50px);
    }

    .right {
        transform: rotateY(90deg) translateZ(50px);
    }

    .top {
        transform: rotateX(90deg) translateZ(50px);
    }

    .bottom {
        transform: rotateX(-90deg) translateZ(50px);
    }

    @keyframes spin {
        from {
            transform: rotateY(0deg);
        }
        to {
            transform: rotateY(360deg);
        }
    }
</style>
