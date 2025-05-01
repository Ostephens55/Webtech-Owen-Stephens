DEV Reflection 
Submit in VS Code: dev-reflection.md

I developed Owen’s Total News Site.

Dev reflection prompts:
How did you interpret and implement someone else’s idea?

Owen (PM) gave me a lot of creative freedom. He gave me categories of news to cover, but no specific layout or source of news to choose from. I chose the ones I thought were most relevant to the category, and did not require a subscription. The NYT on the front embedded with RSS DOES actually require a subscription, but I hope that is okay, because it is one of the most popular news sites that I wanted to feature. Having creative freedom for most all visual design made it very fun to create. 

What were the challenges in development and collaboration?

I wanted to put more news stories embedded directly in the site so that you could carousel through the live updating stream like on the homepage, but I was not able to add any more of these to the news by category tab for free. I decided instead to link them to the live updating page for that news site. I figured this was okay since Owen’s wireframe has links as his possible design suggestion. PM DEV communication was good for the most part. I ran into a little trouble early on. I was not added as a collaborator on the repo until the night before the site V1.0 was due, so I had initially been working in a forked repo that I then merged with the main branch when I was made a collaborator. I got confused because then I kept working in the fork and merging upstream to Owen’s main repo. I hope I made it all work out okay, I think I did.

Which parts did you use AI tools for, and what did you learn from that?

From using the below AI prompt, I learned how to use the localStorage function within the if else statement: 


I followed along in class, and asked copilot the following so I could store theme:

“how can I store the theme "LightTheme" or "DarkTheme" using localstorage so that the last chosen theme will remain on reload or when tab is switched.”
<script>
    const toggleButton = document.getElementById('toggle-theme');
    const themeWrapper = document.getElementById('LightTheme') || document.getElementById('DarkTheme');


    // Check localStorage for the saved theme and apply it
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme) {
        themeWrapper.id = savedTheme;
        toggleButton.textContent = savedTheme === 'LightTheme' ? 'Switch to Dark Theme' : 'Switch to Light Theme';}


    toggleButton.addEventListener('click', () => {
        if (themeWrapper.id === 'LightTheme') {
            themeWrapper.id = 'DarkTheme';
            toggleButton.textContent = 'Switch to Light Theme';
            localStorage.setItem('theme', 'DarkTheme'); // Save the theme to localStorage
        } else {
            themeWrapper.id = 'LightTheme';
            toggleButton.textContent = 'Switch to Dark Theme';
            localStorage.setItem('theme', 'LightTheme'); // Save the theme to localStorage
        }});
</script>



