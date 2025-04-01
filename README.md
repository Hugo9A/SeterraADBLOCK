# SeterraADBLOCK


const blockedUrls = ['https://s1.adform.net/banners/scripts/rmb/Adform.DHTML.js', 'https://track.adform.net/banners/scripts/rmb/Adform.DHTML.js', 'https://track.adform.net/', 'https://ade.googlesyndication.com/', 'https://adserv.snigelweb.com/', 'https://marketplace.anyclip.com/', 'https://aax.amazon-adsystem.com/', 'https://securepubads.g.doubleclick.net/', 'https://adclick.g.doubleclick.net/aclk?nis=4&sa=l&ai=Cmcw9bbqQZ5vvGbya-cAPnJq6SNCyt_B8sdT21LwTru7GrpcOEAEgjr2eHGDxhYCAvB-gAaqZ34ApyAEJqQKKzVYVzDuBPuACAKgDAcgDywSqBJ4CT9B6lkDiWW4VaJ4T_tSINGNUWBwn_-3ir416DG_f3okpFLvXwje7BA0Nk8jEdQgzeMuq5X3KplGU8BEyVxVaEKMggAkyvrxiHY_8ZKJMLElwEudXJwGUk0V46dqpOcFXRgE8HbQhpeSmx7dVqxe2WDvBSWLfJRrlz30tsU_m7qvMGiH9paOWV5a0NoyPciRRQlWvBe11wmjAp_AXLHR8PackRfEIN0y5GuWYACEH8S6EvxHTHYllbS2JVzayF6HjOT0oGmRGxcO-Tvm-tZTnaPKDMC77ALLBiDH4aef420qLKjzpMPgcomaJVPGuLXx4hYIDFgb0wDATRbghtpg5d2lWPsW0H34ynu-Gju7H-M629Mzc16jOVaMSE1zkVsAEhd2X6IQF4AQBiAW5pfqUUvoFBgglEAEYAqAGLoAHuovP-wSoB9m2sQKoB6a-G6gHjs4bqAeT2BuoB_DgG6gH7paxAqgH_p6xAqgHr76xAqgHmgaoB_PRG6gHltgbqAeqm7ECqAfgvbECqAf_nrECqAffn7ECqAfKqbECqAfrpbECqAfqsbECqAeZtbECqAe-t7ECqAf4wrEC2AcAwAgD0ggzCIDhwHAQARgdMgf7goDun4ABOhGB0IOCgICECICAhICAlK7gA0i9_cE6WIeun4WCiYsDgAoDkAsDmAsByAsBgAwB2gwRCgsQsLKUl5DFxdfwARICAQOqDQJTRcgNAeINEwj27p-FgomLAxU8TR4CHRyNDgnqDRMIjK2ghYKJiwMVPE0eAh0cjQ4J2BMM0BUB-BYBgBcBshcCGAG6FwI4AbIYCRICsFMYLiIBANAYAQ&ae=1&ase=2&gclid=EAIaIQobChMI29mghYKJiwMVPE0eAh0cjQ4JEAEYASADEgIbEfD_BwE&num=1&cid=CAQSTgCa7L7dYYD58BaUVt05vyh26pX6Byy9e0QhgdKd9GK0gcu_loDS9LVk5FR1tIIoEvz1xTYtdvTj9WpH5zmYbPKuqE_TTeWkDwW9FQDw9BgB&sig=AOD64_0zR0MnNmvWoZCeJLKBHqYvXcg8MA&client=ca-pub-4276969157128104&nb=9&adurl=https://gp.manygoodapps.com/games/lp_com-coffeestainstudios-goatsimulator-free.html%3Fpid%3D22061843024%26gid%3D%26cid%3D%26k%3D%26dv%3Dc%26gad_source%3D5%26gclid%3DEAIaIQobChMI29mghYKJiwMVPE0eAh0cjQ4JEAEYASADEgIbEfD_BwE', 'geoguessr.com:14193-1743430007626-default'];
window.fetch = new Proxy(window.fetch, {
    apply: (target, thisArg, argArray) => {
        if (blockedUrls.some(url => argArray[0].includes(url))) {
            return new Promise(() => {});
        }
        return target.apply(thisArg, argArray);
    }
});


Paste code into the seterra console upon site refresh
