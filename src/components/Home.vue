<template>
    <div class="home">
        <h1 class="title">Welcome to IE Bank</h1>
        <a role="button" href="/accounts" class="btn btn-primary mt-3">View Accounts</a>
    </div>
</template>

<script>
export default {
    name: "Home",
};
</script>

<style scoped>
/* Background with a solid color */
.home {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    background-color: #ffffff;
    text-align: center;
    animation: fadeIn 2s ease-in-out;
}

/* Large, bold title with a dramatic color */
.title {
    font-size: 4rem;
    font-weight: bold;
    color: #0000ff;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
    margin-bottom: 1.5rem;
    animation: slideIn 1.5s ease-in-out;
}

/* Eye-catching subtitle with a modern font */
.subtitle {
    font-size: 1.8rem;
    color: #f2f2f2;
    font-style: italic;
    margin-bottom: 3rem;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
    animation: slideIn 2s ease-in-out;
}

/* Bold, modern button with neon effect */
.btn-primary {
    background: none;
    border: 2px solid #0000ff;
    color: #0000ff;
    padding: 1rem 2rem;
    font-size: 1.2rem;
    text-transform: uppercase;
    text-decoration: none;
    border-radius: 50px;
    transition: all 0.3s ease-in-out;
    position: relative;
    z-index: 1;
    overflow: hidden;
}

/* Neon glow and hover effects */
.btn-primary::before {
    content: "";
    position: absolute;
    top: 0;
    left: -100%;
    width: 300%;
    height: 100%;
    background: rgba(255, 255, 255, 0.3);
    transform: skewX(-15deg);
    transition: all 0.5s ease-in-out;
}

.btn-primary:hover::before {
    left: 100%;
}

.btn-primary:hover {
    color: #ffffff;
    background-color: #0000ff;
    border-color: #0000ff;
}

/* Animations */
@keyframes fadeIn {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

@keyframes slideIn {
    0% {
        transform: translateY(-50px);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}
</style>