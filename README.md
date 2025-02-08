<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Educational Blog</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: lightblue ;
        }

        header {
            background: lightcoral;
            color: white;
            text-align: center;
            padding: 20px;
        }

        header input {
            width: 80%;
            max-width: 500px;
            padding: 8px;
            margin-top: 10px;
            border: none;
            border-radius: 5px;
        }

        nav {
            display: flex;
            justify-content: center;
            background: lightgreen;
            padding: 12px;
        }

        nav button {
            color: white;
            background: grey;
            border: none;
            padding: 12px 20px;
            margin: 0 10px;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
        }

        nav button:hover {
            background: #0073e6;
        }

        .container {
            width: 90%;
            max-width: 1000px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 5px;
        }

        .section {
            display: none;
            padding: 20px;
        }

        h2 {
            color: #004aad;
            margin-bottom: 10px;
        }

        p {
            color: #555;
            margin-bottom: 10px;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .article {
            background: #06b8e4;
            padding: 15px;
            border-radius: 5px;
            text-align: center;
            border: 1px solid #ddd;
        }

        .article h3 {
            color: #0073e6;
            margin-bottom: 10px;
        }

        .btn {
            display: inline-block;
            background: #0073e6;
            color: white;
            padding: 8px 15px;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 10px;
        }

        .btn:hover {
            background: #005bb5;
        }

        form {
            background: #f9f9f9;
            padding: 15px;
            border-radius: 5px;
            margin-top: 15px;
        }

        input, textarea {
            width: 100%;
            padding: 8px;
            margin: 5px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .author-bio {
            background: #f9f9f9;
            padding: 10px;
            border-left: 4px solid #0073e6;
            margin-top: 15px;
        }

        .footer {
            color: black;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            padding-top: 10px;
            text-align: left;
        }

    </style>
</head>
<body>
    <header>
        <h1>Educational Blog</h1>
        <p>A blog for sharing educational content and articles</p>
        <input type="text" placeholder="Search articles...">
    </header>

    <nav>
        <button onclick="showSection('home')">Home</button>
        <button onclick="showSection('articles')">Articles</button>
        <button onclick="showSection('contact')">Contact</button>
    </nav>

    <div class="container">
        
        <!-- Home Section -->
        <section id="home" class="section">
            <h2>Welcome to the Educational Blog</h2>
            <p>Read articles on various topics and enhance your knowledge.</p>
            <div class="grid-container">
                <div class="article">
                    <h3 style="color: black">ARTICLE</h3>
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS9vGuGZFxaUrziYIkrImJqHQyIahTrve4b5A&s">
                    <h3 style="color:black"><b>TECHNOLOGY</b></h3>
                    <a href="#" class="btn" onclick="showSection('articles')">Read More</a>
        </section>

        <!-- Articles Section -->
        <section style="background-color: lightblue;" id="articles" class="section">
            <h2 style="color:#222">TECHNOLOGY (AI)</h2>
            <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxISEhUSEhIVFhUWFxUWFRUVFxUVFhUVGRUXFxUXFxUYHSggGBolGxgVITEhJSkrMC4uGB8zODMtNygtLisBCgoKDg0OGBAQGi0lHyYrLS0tLS0tLy0tLS0tLS0tLS0rLS0tLS0tLS8tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAKsBJwMBIgACEQEDEQH/xAAcAAACAgMBAQAAAAAAAAAAAAAEBQMGAAIHAQj/xABGEAACAQIEAwUFBAgEBAYDAAABAhEAAwQSITEFQVEGEyJhcTKBkaGxQlLB0QcUI2JyguHwM5Ki8RVDssJTg5Oz0uIWF2P/xAAaAQACAwEBAAAAAAAAAAAAAAABAgADBAUG/8QALBEAAgICAgEDAwMEAwAAAAAAAAECEQMhEjEEIkFRE3HwYZGhMsHR4QWBsf/aAAwDAQACEQMRAD8Aopt1G1imSWCTAGtTDAtyAPoVP0NbOJ5pZRIcPWNZ02py+DYbqR6g0NiLOXcEeulK4jxzNih0rQLRd1aiVaraNcZ6MtpUwSprFqaLGGplEpnlSYvK1qRTFsNULYepxAsqAiK8iims1G1uhRYpoHYVGandahagWRZpWCsit1WoMzU1oaIyVq1uoLYIwrTLRTW687uhQ/IGIrRlos26jZKNEUgWK8IqcrWoWhQ/IGYVEwo24tDOKDRbGRBFakVKWHWsO1KWWQEVoRU5Wo2FQdMirK2IryKA9nleVsRXlAJ5WVlZUIZWVlZUIdcwODznLIBYSSeS/mfp60Y/AyBOYR7vzqLhbRc/kH0Wm5vCunGKo8NlytSqxPc4Y4GhHzHlQ9y/i0ELdeBoFzkrHTKTFP3xukEUruIznQflQlBe4+LPNPQFY4vbKD9YsoW++bCHMORLATNerd4c51RAfLvk/GKixGFZZ0MDciQI/GhlEwJOnUk/WqHjOrHyVW0PcNwzAv7Nwj0uofkyzTBezdsjw3j70B+YalPD0A5DXyA+lPFwqb5RPpz61bHHrsw5fKi5P0g3/wCKuxAV0JOgBzKfoR86V47g72rhtuPEI0GszqIPOrfb4PeWSmdXQBlUtBO32SdfSieJYUteNyD3nd2W7vYkMWDEA9PDQ1YyTcbSa/H/AIKk3ZMjLmuIpYSFMT7tdaCxHZkBzbN2XEeFbV0nXbSPMVdr+DcKFCg6zMwEEGfbjU6THJee1A3cISAjZFyjR+9tZdycpGbNl1OsHUnSDIV0XQ5XVMo7cCU5ouXDlnNFlpEe1IJnTn0pxwL9G365bF2xjrJXYgq4ZG+6y8j9eU1PjbqpeDXGACFGBV7LM+RVGsXIVmKk7mJG8arrHZ83VQgBc8sq5nXQsYJCAlRtGaIA95qavo3Qmo7kiwJ+ha7zxae5G/OpP/04RvjUH8n9ar9rsjcZ8lxVTfxXLz5diRqrHeN/WYg1DZ4CodkaxDISGBZ5BBg/bqRxyfuHJ5OKCtwY74l+jVLIB/Ww5M7KABpInxGqtheEYdlUvjFRiJK92WynvMkZgY28XprtrTp+BW9AbeXnpOvkda3fgFobrl8iza/DUVZ9KRkXm4W7WvvYkPAsPIH60sEkEg2fCA2UMf2moYa6SR9qK9/4JhIk4sAw+k2zqDCzlY6fM00/4FZJ0QHyDv8Aj+FE4LgqEEKAoB2KhjPqf70oLFIaXnYl7WVq9wvCBXjFyw9gZSASFnXQ6FoAjr60ku4YAf4ts+Qzyf8ATXRl4MmbKxGsRFtNyQPgJn+5oQ8OQROUnWYVY2kDbXnR+k/kC82L3xObtXgrqA7F2sZgs1lVS/aa4oI2ufaCt7mAB3Ec65pdw7K5RlIcHKVjWekVUzbF2rRPwjg9/F3VsYdM7tr0VVG7O32VHX6kgV0Cz2FwmEWb4OIujfNK2gegQe0P4p9BVy4Fw6xwPh+e/Hf3QGunSS0SLYP3UGnrJ51zvtF24vtLJg2Fv71zMv1Gnviks2wx8V+pmL4ulvw2rNpF6JbRR8hSy/xGzd/xsPaaeeQK3+dYYfGk9vjPfOFNkqWmMrAjQE8x5VMQfuEerD8JoWPQVd7MYe6pfDs8jXuiwn+ViCT6H41XXsWBoc2m8uPwSrDgbrI0rA95Nb8ZwTXiLogTAfffXxR5jT/eiiudraKuy2B9j4m4foBWueyDHdrP/mn6tTPHYIBdCSRvOx56TzjpSwrqOutSgKf3N++TYWV9yT9Sa1a//wDyX/07Q/CsYVGRUaIpEi41xsI9Mi/IUz7P8Wy3clwMc4AUkloInrtNKu6aYgyK1S8Ldy25BhSTA3NQZO3RP2s/x5jUqCY5mSPoB8Kyl/EsU124zN1gdAAdAKyq2Xro6pw5vGP4Pyp5grGdoO1V/h58a/wHp18qe4fFZB1rqR/pPC5kll2E8R4UbbjNsdYBErqemnn6EUtxFwqGaJPOJHOJg+lWDE3Wu9SZ95kQNB6Ul4jZZQZRlADAyCA3LQ84M0jb9zTGEU249Al28O7JG2UkSfKk1vELlUd2uYfa8XiEk6jNE6xoNgPeTiL/AOzVOq6neB6DnIrThWFzBmInkJ+J/CkNPaGnCwGaIOokwRpz6ab/ADq18BsqtxmaTlRmQHXUQAD6SSPSkHDbfdgEaHTcj3VYsFjAHNxlBzgqQY2Maz7hTbaozpRjJSfyE4W1cZs7S/VR8vdMesVEMUL2dWUfs1L2WbxFABDDX2hA2POD1ky+DZQkE5tIGUkFTEEEaecjpSRLboly+ywAMiA6ZnLCABvoJMdAaMqav9hMKnCfHfzL8/NmPeEz4yBrAt2xt/PTC7xPDlCQpDRIBtrAMjQtJHOlVnijKgi0sgQYcA7b6qTyHPnQGJ4+RAa1PpdfTrsvSkkjXhk17/8Aor4lZXFw6rlctBURlbws5Gk6Qp95HnVs7OoGvXc8yjXSMsTHeQhA/hbSOVVnCYi4XsOLSLbNz2dSSSMuYtA+8Rp5z5e8L45F3IM027roniUSuULlJYFWBE6MBudaq9zZVxX3HuOuw4zG5mW6oIAHdhXDFgTp9lQfIz50Firg78mWEhQ0ATooGxPQD4Vvi8ZiWUJbQKo6rdd2MRmJVMu3KPjS/DWyrAkzPM5pHKDmAPKrse3Zi8puMOI6sW2bWCxAEcyPQfCt7fDGcwQV6lgR/vRHDmh1HVT8Tr+Ap2iVpSOHOck6RWsRwZlPh8Q+fvFZ+qOBrIPrqfWrQ1qgMcPZ9T9NqlL2J9Wa1IS4bhrXnyTuDqx0Xz/pQGLwao8AgmWU69AynSNOXOn9lEFyLns6g9OYBNLOI2rfeSjaZhA1giRO/Lell2X4Jem9Xfzv9gbhvFLuHF23byiWe5mMT4Qq5QG8IBgSx21obhnDv1vieFe7DMLqOWARcyd1cvIGCeEw1oa9G51pirDG8rBssZmYxPhKhiI57H41YP0fYJjjzcJYqLTGGGUqwKoARtszR6mseSPZ6HxclygvsJ/0r8YZr7BNe7KW7c6qrEyXI8tT7hXOrxS3Di7c77TMt2Rmza5SsZcpGmkRPOrd25vtaxF14nLeVzzhQ0kxzA00qmcUtOGF8Bcrl2MlWhnbM66GT4piQNwaznaEpTusSrJ7OZWXyVtY+oq23LVVXF4jNdVOYKqfUtJ+BNW0vRRGR27dG2tivUEe/l84oe21SXbmmnyoivoVsxK3M0RGm0kxzjfWI5zSi8gDKNZjxA8jAp5ibjwCLTkxpIaF5bbfCkdy0wcZwQTJ1FMZIsxgv9/71DIGw160Q9vzHzFQFNf7+QosMTQR50NxEez6Hf3UaAPun+/dQvEpJBPQ/hSvotxv1ICve03qfrWV7f8Aab1P1rKrNR1Th5Gdf4T+NNJpHw6740/hb/upuHrpwejwvlRfP/otXDi3dlVmSVDQRqIMD4z8qYdpsQO6YFSEykjNp4oEADlqcs/vUgwuKAtm5mhhGkAgyDMg7jy86WcY4s7DKsKp3VVAz67N1E8vfvSNWaoT4pb7X5/srmIOpp1wnEZUIGgcDT0j8t6S4hQZK7cxzH5jz/ssLVghVJBmAJ25bUrL4JpD+z4lmJA3I/MUXhro+0edBYbFZbTKTq2vrIy/191b2LgEv92Avmx2+GpoplGSKdDK/wAUuWJW3cI1jUBhIPRgQN/nSW9xO7euA3WL5ScoMADaQANBIHIbgVDevTpMiZojDYDYsY5xty0E9aZpdlcZy3FN18Xo1wyBpYSNdRpPX86jx2DUyMxkSIJB3BExHnTDHPZygeIgnXKIWRy86r/E1LXCQCCSInQ7Ab0rRfCVaNGS8igBwQCMoiCIIJjWOg99IeH3WF095M94C2gnXQnxabDnpTC7iLinQkhdNY1jc+es1rhriXmZYhgQQehk7eVUPs6MNxZYLWRo8CeUhJA/8oiR51OreJTEciPEBy2zE0fwFHtBM6EgqWcqniL52yEhQSRlAgHafOveM4RlKsxAbXMpUKzTJDnKI1Xr91pqzG6Zl8pcoukEWLuVlM6Qp9QNPwNWbDsKqdjVeRI1EEExz26Gn3C2JQBt+X8MkDfzBHurUcSUXdpdDzDX7eXK67Nqw5zrrz5igcVw93APhXMSUGpBH2QT94iDHnHKoAnjIWJOkzAPnrt1o7irXL6pbtX1VbrgLcVQ+UBSYWD1WNKzzvG1xZ2fF+n5kZLLHSpJ1Tt67X5vYoFtrVxbj2yyKZMQQQBr8N9aQcdxtt71y4ilZOg0+7E6bEnWnfDcPhxduAMLlwHLcuC4WuejMGlT5aV5x/gdso120sEA5lAkbHxDzqRzJv1dkz/8XLFjf0ncbtp9/v8A2K3xEMXti2BmJgA7RLK0+UZasfYSy/62CjL3QtXAwWd8ySDPOSCD0BpTYCC5ZNwkLDAt9xjBBbos6H1qy9jrdxMTdRkcBbZzOxkMSVKC31WA+u+22tJlfZd4UfVB/qU/t3gJvues1x7HOtq8ylII+0uu4kMFJifh+Nd67cJu1cA4uc993n7ZAj90CszO+uzzhyL3q7GDOcTG06zsZge+rAbxFKeC4cXWK32aIBLMWYICuZWKDVpkDymvMZf7rKFuhpBlWUnLDEDXcyNaCCxwmIorDK1wmJAHMAnU7bVV/wDi56D4GrPwDFW3wzC6BmAYhsoUmWOgP2oEQTrrGukNHbKc7cYNogxdkKYa8w5wVP50kxVxgylTmMnfpT3F3MLFkSdx3hEyOs9delBcQNjv07v2NM2kDcTvTsz41oBe5diY0PPl9KiJukTGnXl9Kf35hyZy5TMxB6ZffHvoYHaJywNoyxGs/OoSLXwLLTXTsJ9CfyoTGsxPi6aelWHDZSoy/eO0deeblSrjYGfTag1oaEvX0KMT7Tep+teVtih4j6n61lVG1dF+4c4z29eTf99Og1VzAt47f83T97+9afIa6GN6PIeZH1r7EoxBWYiDuDsakvWzcBIMeUTrGutCXanwGN5EDQz5Ec6MtCYY20hPflG6EVZuC5cT1yWlJdRoZYwoXrLkegk0g7QYgFtABJO3IdPnRvYrHRfNoqB3oCjcjMpzBSGOxgjcbiqWzowg1ouGJd8k9zaFskKBk0kaAZvanzmaWY8qotvaEI2eUOuVwFzCSfEIKkevrTLFcRt5YLXFZWzG2ECgNBWCSTl9PXShON4pDaAZSHds4GhypGkaDLJ5dADzq0wNttpu/wA/j7C7B2czDoBmP4VtxHEktkG31M7URwi2uVjm+Ijb0nrQdmwXuAAgyY3A0n94jlRsTi0l+owwoEagGR1IAE6OxHTkOc+evt18viXPpsUCos+Qg0bhcPmZVOxhm9/sj0A5VasN2ZXUu0/w6fX6Urpdl2KM5OoI5fiVVg2XXTUABXEbGBo4HTQ1WrymzdOUgtAIcaryIKTv6/711PtZ2XFq2bqPqGEACOp3nyrnXFbeYBwORMdNcrgDpOVvKTVMl7o34W9xkqY0TijmzmCKwEEq8mI00ykFdPjFTDiN25lcqsLlELOgEhV1J01YerGdTSDB8SK5VAEEwdCTqRvyp01wlgiL9mYAVQqyCSTPVVEmKMWLmjcXQ5sSp20BkcpU7fKPjR+Dx+QEA6A6MFDGOhBIj3dTSprhRZzWyAIJVs0dJETGwmIpbe4jamc8n90E+VaOSo5Kwy5aRazxtHM92WMj9mdmXzI5RRtjGvexWZCqYdEDKp1db+bnBiIn8d4rnj8dSYL3G5R/Qmj8HxZt0sXT5wfwGlJLjP32asH1PHv0pxbtp/jDe0HAbmCb/iNi4CLIm6v/AIlqRmU+cbedX7BYtWA6MPiCPyrnWIxN3EL3GJs3BYcr3mR8rlQwMEncSNR0mKsHFOIMHtWcMge68lIMW0tJGZ3I+yJAA3JIGlZZRcTv+P5EMy138BGHUJi0ttB8d1cuhlHV8sjoVI+NO8NjbeDYpcueAQbSnVghJUoDMtB2nUAjeJpZw97T37T4piLtsEAqAqsfsk7mFJJAJO+s0h/SzjXsvYKMpzpcE7xBGV1PI+I+/eYFM5cmZlgeCLr50Nu3mzAfHyrgGPXJcIM+0W9xG9dj4RxH9Y4daZjL281h+vgANs/+myCeoNc643wi/mc+xbjfNEruZA166VU0dOMr2VbiMhlO37O1/wC2oP0rxEJJJWdJ8WmkRm9Jqfj9sC6SNm8Q9MxH4URiLyOoJJTw775pIkeca0o7fQ8weCKm0O4tp95u7xCM0I25u+E6xMDmNqIvpp8Ki4bibQ07xrrQT3jrcTTTQB2PUbRtsakv3RET8/wrTjXpOR5cm8onxCeL/eh5yshidduu1FXzr/vXmBZO8UMQPa32nLpPqYpWXQegh8asa2TAjloN45etDnHW9u7+X9KYrdImTIaI1BnXl8vhQ2JEzofh/T8ajBFIht4leSFf5T+VBY+CdBEVYOFqi3SHkRp56TpJ84oDjyqbvgj2RPSdZ/Co1okZesr+LTxH1P1r2t8XqSR1P1rKpZui9FmwVzxW/VulPkuUHwrhcYJsU4El0W3p9nvAHb3nT3HrW1pp0rZiejz/AJmP1L7BNy5UWFbx+41FcuGoUvhWljA139KaTKMMKYNj72dyfh6VHaMMpzbEbTprWjEf7a153qj+pFVWjcouui1YbtHiBu4OXQZkVyANBDMCRGnOvcViXcl2bMTqSSJP40ks3JkqCQefIc99qNvX1yqxaJWIUZtV8O8xyB99MmjNkhOXY94PeOVh5/hWmAJ7xQBJLZdNTqQBSrhPEQHgD2huxnUeQ259aIxT3JMTl0Omg/qfzpuRU8TVFxwV3xDzVfUEDKR8Qa6BhMRntBhvpPqNxXJ+H4jOgbNBzQD++RLJPn7Q9as/BOLXLbBSrEsuYI3hLLJAYT7I0Op009Kk6cR/G5wyulaa/GWDtXaZ7RVEJ3eZUezusHfTp0rjuMsCGBaBmu7DN9lNIkfay612W1iHceLKCGkAGQFKgFTp1B+Nck7S2XsYg2cgEHMs+KbZYtnk7yYUfwHpVF6o6c8b5fU+exM3BLU/4l0+mUU54LatsZKP/iItyGmUWWCwANyWP8g6UsvcQcAkGPQAfhQHBePXLdwkszKTOXNzElSAdDEnTmCR5iRasTLFyjSZ07F2LbAEW2Y5yVLqFUWz/wAs66jyqu4nh9m2xVnw6AFgCz2iSATBiSaBv8dVFVs+ckOBb7uAfGGIuE/ZnpPTTcVNsRMBjuSSx1IJOp8/Mc/nVsp/Bjx+O3/U/wCS5fruETfGWx5Il9vogHzoi32hwS/bvv8Aw2lQfFrh+lc2uvDEAgiTBAgETvHKiLFylU2Wz8WFbRfL/a/Dj2cPdb+K6i/9NufnTXsP2vwr3ntXbaYdrgUWnLMwYyZR2Y+EnwxsCR6VzJ2oS6aE22izx4RxyUkkfQ/FOFBpBGtVriOD8HdYi2LtrlPtIeqNupqtdhv0iNYy4fGFrljQJc1a5ZHQ83Ty3HKdq6u2GS6gdCrowlWUgqwOxBqno60ZRmjj+L4Vi8Gr3MC3f2Ghntsua4hAOrIILQPtL7wKqV/tViL+dH7sK1u9IVY/5Tnck9K7bxLhQtHOr5CNuvwrnvbGxhrgZxay4nKwFxIVHzKUbvU5nKx1GsxOlBhjFLRzfG5j448B0ViBqdZj3hv7NQIlxxCBmA5KCYk6aetP+LKRh0tKCciEE9WZ2dz6eKPcKr+HPhYZ8u3XxeWnxpS1DfAXb6sGY3CieEqWIER7ME7aDSOQpjd4onO1/qH/AMaUYRvBmgxv0BgGfWmXBMZhXupbvWZDsFzB3BE6bTVkZUjLlwc5WB3sdb/8Nv8AMp/7aGDWCSYuDyBQgfIVab/C8BdH7Nbto8mDFv8AMrkz7iPWkOL7P37ZMAMnK4GUK3+Ygz1FBsdY0loBum39kv5yFHzBP0ocsOrD4H8RRy8JuHmo9T+QoXG4B7erAR1BkUGPFG1m7++3w/8AtRDXZEfEnc0vQ1LnoplcobPbteVqTXtAK0df4Bw5sTwpbSEBoZlnbMl4soPSSI+NVlcDiCfZVdtGaYPOcs1L2Z7dthMP3PcC4QxKtny6HWCIM6k/Ghbna5z7Fmyvrnc/6mj5VYm0Yp409sPwfA7juoe4AJ1CgmQNWAzGAYB1irVgezLtbJQXMozzkItquVQwGUe1J3mSfXWqHhe0+J7xW7yFUh2VVVAyrqVJQAwfZ3500wnbErbZTcU5iWi8LzsmYZCqkSCAOZ/pRsR43qv4JeLcFwlsq7sgLTKs6gBgdYGboVMBdJoMYvCIIRrcfuoXP+oAH3VWMfig7DKCFUQJ3OsliBsT05AASYmvLEc6BY00lZZr/FbbqJFx+XiIXzHX+xWtu8ptsq21BBzKSSxgwGjlMZTtyNKrHwBqSSPUfTnToyS7CsLdyuCx0BnQwAfd7qsqNIknTn+QqoLbnbbmenkOp/vQa0wwPE/sNoo0XWY9Tz9fwopiuBZuAogxdsuua14pt8jCsyqRzBYCetWvDYRLNlDbk5gSzMxZi2YyCx5Azp+ZqlYd9mBIIMggwR0IIqwcK4s93NZuNJMvbMD2xqw0+8JPqvnQkn2XeLkinwfbY4scQg70D2vwjYm0rIuZ7eYwIkpEtvvEAx6xvSjE4kodacYC4z2m0I8LQQJI0MEDcmqmzo8LVHKOKYoBco3P9PwoHDxzn+tbcR4XctBHLrcR5y3EzZZG6kMAVbmQes1HhW5jbQx58hRTMs40hxeAELHsqB7zJb5kj3Uvu+1sDA2oq0Z39T/f970Biec8yTPvqxmbGtsGusJ0qewaEIpz2c4Pexd5bFhczt7lVebMeSj+mpIFIjRKOqRPwfh13EXBZsoXdtgPmSdgBzJrXjvCruFum1eWGHTUEdQeYruvZ/gdjhtru7XiuMB3t4iGc9B91RyX6nWqn+kbCrdQOXRPstcecqjcOYRjI12HlsanMsXia72ctwGFe6627alnchVUbkmuu8BC8Lsm099nZyC4Etbttz7sAab6tpMDSuZYL9X4feS/b4uHccsPauXWdToyFbmRFBGntTSPtDdvXbrn9aN0MxYTNuZkgBCTAEwKRzsuxePwdvs7Le45hcQxti6pf7sw3rFUnjWGKvEyORrnWHxbKQDo6HwuNGU9PMVe7XExfto53IEjodj85oJmhqjUWRFLcVwm3M5F130505WtbizRAK7GEUDKFWOhUEa76EUxwpyeyFX+FVX6CvVtVvlqEA7tuGkc62vpnttbJiRoeatyI/vaamuCtIqEOeXiwYhpkEgzrqKKw2IOV0M5Sp0PI8oovjGHAxDagZoaTsBHiPxBrTGYPKi3EYsjyASsajz2I0PpSDgSCtjXiV61MVPs8rK8rKBA5TUq0OhqYGnRmkgmYTzYx/Kup+Jj/KaFY0TjiucqjZkXwq0FcwH2sp1EmTB60IxqAoxTRNo0IDUyPURJoaWJbqSdABqTRnctPiBUqAWzAgxyMHc+XP40d2WwqsurhMwZmb7yhgoQnpoT7x0FNeMYZVtBVulhDXAJH7NwBO06kSsc/hVqWrME5JT4lXvXRsBC9OY856/7VEF2jb739+XKtnXmN+Y/L8qjs3ysxGu6nVW9xoDrYxwOMdF0Ok7Hb+lFDjJUhoIYEEEHYg6HWly37ZAGqEawZZT7/aHwNC3bsztr5jz6016EWN8rL32YxR4jjlLjLbs2zcNsRDXJVVJ66sSByyirVj8M9ls9vbmK5R2W7Q/qWJF0iUZclwArOUwZAncEA/HrXacNi7d+2rowdHEqw1BFUPs6+JuUdlL7TcETF2Lr2AVvZkuG2oBDuphioOzFGbQblVrmlkoDqX0JEFQDPOfF8vdXbcVw0qc6aGq12g7N2sYxuKRaxMe0fYuHlnA5/vD3g1EwTx2tFIRkAjxE7nUD86BxjKScgIXTRiGMwJ1AHOeW1T8Q4bdwz93eQo41B3DDqrbMPMVP2f4Dfx14WLCyx1ZjottebOeQ+uwqxvRgUGpUA8H4VexV5bFhC9xzoBsBzZj9lRzNfQXZvs9Z4Vh+7UhrzgG9d5sfur0Qch7+dEdmuz2G4VZKWvFdYDvbzAZnP/ao5L9TJpPxniuYnWq7s6EMajv3JMXj5O9V/tVF3DXEPMEfEEfjUV7HUBjseCsen1qDnHMD7Rb7oJHryq29nOHpiTds91bi2pL3GnvC4MBlfcag6baDSqrdTurrodgWQ+kxTOxxUopyoouMuU3cxgg7sV5t6mKRFjAsLhe+uhS6ppq5kiROunpT7hNvu4TNmgnUbHU7eVVRvE0DyAqzcKMe4QKKAywhq3BoFb9TW7lMKAcU7Q27TFAMzDeNgfWlT9rH5Wx8aR48zduH99v+o1BSWPRcOG8fF1ghEE7dDTdmqj8EeLy68x9at1+7TJitCztDcnIrH9mSc0AEgiIYc+dBcS4gDZtWFfOtvMQ2XLvMDqYk1LxLK8FrgULOm7GY2FJGM0GE9U1JUarUy0UVyNMtZW5NZUFs3FSpUJNbo1EraJ4qN63zVG5osSJHUizUObWpBcEUCxoecG4n3cBhIBJWApIP8LaMpgaH16gu8TxzvJ8OYsAGdwFaAZGUIYBncmZ+tPsNTCzdqyLMWaG79xumDR1kMVM7HUf5h+VD38DGp1H31gj3xp9DW2FveH3ms70jYkeY0NWNIyKUk2gV8NA0afLT6GhLgPNfrTPGXc4ZjEwAIAXQCBoBvAEncnUyTSp9Jgnafp+dJI04m2CXh0U/M/Sn/Yjtc+BfJc1w7HxLzQn7ajf1HP1qv39YknX8yPwoGRp66+mn9apZ0cXR9NWMQtxA6MGVgCrAyCDsQaXcRwYOo0Ncs/Rt2v8A1ZhhrzfsHPgY/wDKcn5ITv0OvWujdr+K/q2Eu3eYEL/Exyg+6Z91AuFp4hbxTjAPbW8zEwNZtgaNczj/AAwOvPbWYq7cCwmG4bY7mxqTrcuNGe43UkchsBy+Ncx7G41MPhg4M3bwzXH5xJypPQD5yaYYjj086ItK7LRxjjczrVQ4hxTzpXjuLTzpFisaTzohGuJ4p50sxHFfOld6+TQ5HWgTS7C+LcJ71zdRh4oJB9NwRSi7gwPCDJ5nlV44v2Xt2sHZv23d++tpcJOgUsPEgA6GRudqpcRpQaGTPcPYC+vWj7DxQamibVQgys3KLtPS60aIZ4Vj0BPwFEBTnaST1M1rWVlIOMOCD9qvr/WnnEsTlUn+5pTwC34i3QH8q143flgvTU+p/p9aZdCvsCdyxk7msrUGvZqAJBWZq1DVqTUFo2L1lRE1lCxuITmrFaoc1ehqNicQsXK1d6gDVjGjYqgYzV6rVCTXqmgWcQ+09EpdpdbNTqadMzzghth8Rp76k78UnmvabkZ3gTY2u3xB9KWvdqEmo2ag5WPjwqJ5eahWqVzUJNVs2QVHoNWfEdpHv4AYS4ZdHUox+1bCsMrHqDl15j01q4qVKgz0N8BjjaUIScvLynUj0maKPEj1pJmrQ3CKIvKxw+JJqJ36mln6w3WsVqBGw43RWjXKGL1Gz01lXBy7OxdjLIxfBXTdsPduJ/K0XR83b4Vy7iFnK5HnXQ/0FYqVx+HJ9q1bugfwllY/61+FU7tLYi+48zQL1oT26LtCorVujLVmgE3t0Vbt5vCdiCPiIrRLVT2xFEBVr/CLymMhPmNRW1jgt5vsQOpq5hxWjXqHENiy1ghYt+fM1Vb1zMxbqZq28Xu/sn/hPzEVTqjIjeaya0rKFho3zV4TWtZUJRlZWVlAJsK2FeCt1oitmVjGt61aiKRGvVrw1i0Bwu1RKihbVErTozTN4rCK8ryiVHhqC4alah3oMtgiNzUJNbvUdIzRFHoNTWzUFS26iJLoIqFzW9RPRYkUYDUq1CKlSogyNmqImpGqI1ARLv8Aoc4otjiSBzC37dzDydszgNbHvdVHqRUvbWxF9vU1VOzLlcZhiDBF+wQehF1Yq+/pZw628fdVBlWQYExJAJjprUQ5T7a0XbpYtw9akW83WoQaZq173Wlxut1rayZOtGwUMWxNQviqKRABoBUONUFdRRIK+KYsG2ROpj60iqXEHxGoqRsZGVlZWUAmVlZWVCGVlZWVCH//2Q==">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTGRGawbXPNl4bE1k22BkjivRHBDvWad_rlRw&s">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRYTz5b0VHp3jCQ0jUAPQSIur3ZSOZ8UTcUrg&s" width="300px">
            <p>Artificial Intelligence (AI) is revolutionizing various industries, and education is no exception. From personalized learning experiences to automated grading systems, AI is transforming how students learn and teachers teach.</p>

               <H5> 1. Personalized Learning </H5>
               <BR>
                <P>
                AI-powered systems analyze student performance and create customized learning plans based on strengths and weaknesses. This helps students learn at their own pace and improve in areas where they struggle.
                </P>
                <BR>
                <H5>2. Smart Tutors</H5>
                <BR>
                <P>
                AI-driven virtual tutors provide real-time assistance to students. These tutors can answer questions, explain concepts, and guide students through complex topics, reducing the need for additional tutoring services.
                </P>
                <BR>
                <H5>3. Automated Grading </H5>
                <BR>
                    <p>
                Grading assignments and exams can be time-consuming for teachers. AI-based grading tools help evaluate multiple-choice tests, essays, and reports quickly, saving time and ensuring fair assessment.
                </p>
                <BR>

                <H5>4. AI in Classrooms </H5>
                <BR>
                    <P>
                Many classrooms now use AI-powered tools like speech-to-text software, translation apps, and virtual reality simulations. These tools help students with disabilities, language barriers, and interactive learning experiences.
                </P>
                <BR>

                <H5> 5. Future of AI in Education </H5>
                <BR>
                    <P>
                
                AI will continue to evolve, making education more accessible, efficient, and engaging. In the future, AI may help create fully automated, intelligent classrooms with virtual teachers and adaptive learning systems.
                </P>
                <BR><BR>
                <H4>CONCLUSION</H4>
                <BR>
                    <P>
                
                AI is reshaping education by making learning personalized, efficient, and accessible. While challenges like data privacy and ethical concerns exist, the benefits of AI in education outweigh the drawbacks. Embracing AI will lead to a smarter and more innovative education system.</p>
            </P>
            <BR><BR>
            <div class="author-bio">
                <h3><U>About the Author</U></h3>
            <BR><BR>

                <p>JORAWAR SINGH is a passionate writer and tech enthusiast who loves exploring the latest advancements in education and gains the knowledge of technology that is widely growing all around the world ,mainly about the topic of <B>ARTIFICIAL INTELLIGENCE AI</B></p>
            </div>
            <br><br>

            <h3>Leave a Comment</h3>
            <form>
                <label>Name:</label>
                <input type="text" required><br>
                <label>Comment:</label><br>
                <textarea required></textarea><br>
                <input type="checkbox">I agree to the terms and conditions.<br>
                <button type="submit" class="btn">Post Comment</button>
            </form>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="section">
         <img src="data:image/png;base64,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" width="250px">
            <form>
                <label>Name:</label>
                <input type="text" required><br>
                
                <label>Email:</label>
                <input type="email" required><br>

                <label>Message:</label><br>
                <textarea required></textarea><br>

                <h3>How did you find us?</h3>
                <input type="radio" name="source">Google<br>
                <input type="radio" name="source">Social Media<br>
                <input type="radio" name="source">Friends<br>

                <h3>Topics You Like:</h3>
            
               <input type="checkbox">Technology<br></li>
               <input type="checkbox">Science<br></li>
               <input type="checkbox">History<br></li>
    
<br><br>
                <button type="submit" class="btn">Send Message</button>

            </form>
            <div class="footer">
               <h5 style="text-align: center;"> Contact Me</h5>
               <h5 style="text-align: center;">joravarsingh2546@gmail.com</h5>
            </div>
               
                

        </section>

    </div>

    <script>
        function showSection(sectionId) {
            let sections = document.querySelectorAll(".section");
            sections.forEach(section => {
                section.style.display = "none";
            });
            document.getElementById(sectionId).style.display = "block";
        }
        // Show home section by default
        showSection("home");
    </script>

</body>
</html>
