<script lang="ts">
    import Panel from "./Panel.svelte";

    const expData = [
        {
            title: "Freelance Full-stack Developer",
            timePeriod: "Jan 2014 - Jan 2016",
            description: "Managed various projects, including an admin panel for educators, landing pages, 1CBitrix plugins, and webpages with custom CMS.",
            tech: "JavaScript, Typescript, CoffeeScript, jQuery, Angular, Grunt, Ruby on Rails, PHP5, MySQL."
        },
        {
            title: "Full-stack Developer, LightPoint / MG2 Subscription Panel",
            timePeriod: "Jan 2016 - Jan 2017",
            description: "Crafted subscription applications tailored for US-based print publishers.",
            tech: "JavaScript, Typescript, NodeJS, jQuery, Less, Grunt, Pug (Jade), Knockout JS."
        },
        {
            title: "Full-stack Developer, Instinctools / Internal",
            timePeriod: "Feb 2017 - Mar 2017",
            description: "Involved in internal projects for Instinctools.",
            tech: "React/Redux, Node.js/Express."
        },
        {
            title: "Full-stack Developer, Instinctools / Oakley",
            timePeriod: "Apr 2017 - Jun 2017",
            description: "Assisted in developing a platform for selling customizable glasses, with a focus on lens customization.",
            tech: "Java/Hybris, JavaScript, Gulp, Sass."
        },
        {
            title: "Front-end Developer, Instinctools / Skype TripAdvisor Add-in",
            timePeriod: "Jul 2017",
            description: "Established the I18n layer for the app, ensuring correct language, numbers, and time formatting.",
            tech: "React, CRA."
        },
        {
            title: "Front-end Developer, Instinctools / Event widget",
            timePeriod: "Aug 2017",
            description: "Created an event booking widget, a standalone application suitable for any website.",
            tech: "Preact, moment, webpack."
        },
        {
            title: "Full-stack Developer, Instinctools / Mobaloo",
            timePeriod: "Sep 2017 - Feb 2018",
            description: "Contributed to a concrete delivery project for construction sites, primarily on the backend.",
            tech: "Node.js/Express, MySQL, AWS."
        },
        {
            title: "Front-End Developer, Instinctools / Lightning system",
            timePeriod: "Mar 2018 - May 2018",
            description: "Developed tools for creating schemas to control lighting systems in buildings.",
            tech: "React, sass, canvas."
        },
        {
            title: "Mobile Developer, Instinctools / Drop boy",
            timePeriod: "Jun 2018 - Aug 2018",
            description: "Developed a mobile app for courier delivery tracking using react-native, featuring text recognition for Bar and QR codes, and signature capturing.",
            tech: "React-native."
        },
        {
            title: "Full-stack Developer, Instinctools / Uber web",
            timePeriod: "Aug 2018 - June 2020",
            description: "Contributed to the main Uber website and internal microservices.\n Notable Contribution: /price-estimate",
            tech: "Fusion.js, Custom Uber React framework, GoLang, Styletron, Storybook."
        },
        {
            title: "Full-stack Developer, Oxagile / Shindig",
            timePeriod: "Jul 2020 - March 2022",
            description: "Worked on a video chat platform supporting multiple speakers and numerous users.",
            tech: "Angular 1.4, Node.js/Express/Nest.js, MySQL, Redis, AWS, Docker."
        },
        {
            title: "Front-end Developer, Oxagile / Gousto",
            timePeriod: "Apr 2022 - Nov 2022",
            description: "Engaged in developing a food delivery website based on subscription.",
            tech: "React/Redux, postcss, emotion, swr."
        },
        {
            title: "Full-stack Developer, Oxagile / Opera",
            timePeriod: "Dec 2022 - June 2023",
            description: "Led the development of the web gaming platform Game Bites.",
            tech: "Svelte-kit, Docker, Strapi."
        },
        {
            title: "Front-end Developer, Oxagile / Opera",
            timePeriod: "Dec 2022 - June 2023",
            description: "Tasked with bug fixes for the Aria browser extension.",
            tech: "React, Redux, Tailwindcss."
        }
    ]
</script>

<Panel>
    <h3 class="text-xl font-bold">Professional Experience</h3>
    {#each expData as job}
        <table class="table-fixed border-collapse text-left my-4">
            <thead>
                <tr>
                    <th class="py-2 bg-slate-100" colspan="2">{job.title}</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td colspan="2"><i>{job.timePeriod}</i></td>
                </tr>
                <tr>
                    <th class="w-24">Description</th>
                    <td>{job.description}</td>
                </tr>
                <tr>
                    <th class="w-24">Tech</th>
                    <td>{job.tech}</td>
                </tr>
            </tbody>
        </table>
    {/each}
</Panel>
