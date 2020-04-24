<template>
    <div id="snippet_wrapper">
        <polaris-card title="Google search engine preview">
            <div id="cnt" class=" mdm mdm">
                <div class="mw">
                    <div id="rcnt" style="clear:both;position:relative;zoom:1">
                        <div class="col" style="width:0">
                            <div id="center_col">
                                <div class="med" id="res" role="main">
                                    <div class="g">
                                        <div class="rc">
                                            <div class="r">
                                                <a href="javascript:void(0)">
                                                    <h3 class="LC20lb">{{title}}</h3>
                                                    <br>
                                                    <div class="TbwUpd"><cite class="iUh30">https://{{shop}}/.../example-link-from-your-stor...</cite></div>
                                                </a>
                                            </div>
                                            <div class="s">
                                                <span class="st">{{desc}}</span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </polaris-card>
    </div>
</template>

<script>
    export default {
        data () {
            return {
                shop: '',
            }
        },
        props: {
            obj: Object
        },
        created() {
            if (window.buymaxx.shop_data.domain.length > 0) {
                this.shop = window.buymaxx.shop_data.domain;
            } else {
                this.shop = window.buymaxx.shop;
            }
        },
        computed: {
            desc: function () {
                return this.obj.desc.length > 200 ? this.obj.desc.substring(0, 200) + '...' : this.obj.desc;
            },
            title: function () {
                return this.obj.title.length > 70 ? this.obj.title.substring(0, 63) + '...' : this.obj.title;
            }
        }
    }
</script>

<style lang="scss">
    #snippet_wrapper {
        box-shadow: 0 0 0 1px rgba(63,63,68,0.05), 0 1px 3px 0 rgba(63,63,68,0.15);
        border-radius: 4px;
        background: #fff;
        margin-top: 20px;
        #cnt {
            color: #000;
            margin: 0;
            background: #fff;
            color: #222;
        }

        .ts td {
            padding: 0;
        }

        .g {
            line-height: 1.2;
            text-align: left;
        }

        a:visited {
            color: #609;
        }

        .s {
            max-width: 48em;
        }

        .f a:link {
            color: #777;
            line-height: 1.54;
        }

        .c h2 {
            color: #666;
        }

        .mslg cite {
            display: none;
        }

        h1,li,ol,ul {
            margin: 0;
            padding: 0;
        }

        .g,#cnt,h1,html,input {
            font-family: arial,sans-serif;
            font-size: small;
        }

        .c h2,h1 {
            font-weight: 400;
        }

        .blk a {
            color: #000;
        }

        #nav a {
            display: block;
        }

        #nav td {
            padding: 0;
            text-align: center;
        }

        .med,h3 {
            font-size: medium;
            font-weight: 400;
            margin: 0;
            padding: 0;
        }

        #res h3 {
            color: rgb(26, 13, 171);
            font-size: 18px;
            line-height: 1.33;
        }

        .slk div {
            padding-left: 12px;
            text-indent: -10px;
        }

        #cnt {
            clear: both;
        }

        #res {
            padding-right: 1em;
            margin: 0 16px;
        }

        ol li {
            list-style: none;
        }

        .sm li {
            margin: 0;
        }

        #foot a {
            white-space: nowrap;
        }

        #foot #navcnt a {
            color: #4285f4;
            font-weight: 400;
        }

        .r {
            font-weight: 400;
            margin: 0;
        }

        .r {
            font-size: medium;
        }

        h4.r {
            font-size: small;
        }

        .mslg>td {
            padding-right: 6px;
            padding-top: 4px;
        }

        #res h3.r {
            display: block;
            overflow: hidden;
            text-overflow: ellipsis;
            -webkit-text-overflow: ellipsis;
            white-space: nowrap;
        }

        em {
            font-weight: 700;
            font-style: normal;
        }

        li,ol,ul {
            border: 0;
            margin: 0;
            padding: 0;
        }

        .g {
            margin-top: 30px;
            margin-bottom: 30px;
        }

        #cnt {
            min-width: 833px;
            margin-left: 0;
        }

        .mw {
            max-width: 1197px;
        }

        .big .mw {
            max-width: 1280px;
        }

        #cnt #center_col {
            width: 632px;
        }

        .col {
            float: left;
            margin-bottom: 5%;
        }

        #center_col {
            position: relative;
        }

        #center_col {
            margin-left: 138px;
            margin-right: 264px;
        }

        .mdm #center_col {
            margin-left: 138px;
        }

        .big #center_col {
            margin-left: 138px;
        }

        #center_col {
            clear: both;
        }

        #res {
            border: 0;
            margin: 0;
            padding: 0 20px;
        }

        #ires {
            margin-top: 6px;
        }

        #cdr_opt label {
            display: block;
            font-weight: 400;
            margin-right: 2px;
            white-space: nowrap;
        }

        a:link {
            cursor: pointer;
        }

        #appbar a,#tsf a,.bc a,.blg a,.flt,.gl a,.osl a,.slk a,a.fl,a.flt u,a.gl,a.mblink {
            text-decoration: none;
        }

        #tsf a:hover,.bc a:hover,.blg a:hover,.flt:hover,.gl a:hover,.osl a:hover,.slk a:hover,.tbotu:hover,a.fl:hover,a.flt:hover u,a.gl:hover,a.mblink:hover {
            text-decoration: underline;
        }

        #res a,#rhs a,#tads a,#tadsb a,#taw a {
            text-decoration: none;
        }

        #botstuff a,#brs a,#nav a.pn,#nycntg a:hover,#rhs .gl a,#tbpi,.fl,.flt:hover u,.mlocsel span,.navend span,.nsa,.tbotu:hover,.tbt a {
            text-decoration: none;
        }

        #ss-box a:hover {
            text-decoration: none;
        }

        .osl a {
            line-height: 1.54;
        }

        .mi:hover * {
            color: #fff!important;
        }

        #bfl a,#fll a {
            color: #1a0dab;
            margin: 0 12px;
            text-decoration: none;
        }

        .s {
            color: #545454;
        }

        .s .st em,.st.s.std em {
            color: #6a6a6a;
        }

        .s a:visited em {
            color: #609;
        }

        .s a:active em {
            color: #dd4b39;
        }

        .st {
            line-height: 1.54;
            word-wrap: break-word;
        }

        #rcnt {
            margin-top: 0;
        }

        #ab_name a {
            color: #999;
        }

        #ab_shopping a {
            color: #dd4b39;
        }

        .ab_button:hover>span.ab_icon {
            opacity: .9;
        }

        #set_location_section a,.tbou>a.q,.tbt label {
            color: #222;
        }

        #obsmtc a,.rscontainer a {
            text-decoration: none;
        }

        .currency input[type=text] {
            background-color: #fff;
            border: 1px solid #d9d9d9;
            border-top: 1px solid silver;
            box-sizing: border-box;
            color: #333;
            display: inline-block;
            height: 29px;
            line-height: 27px;
            padding-left: 8px;
            vertical-align: top;
            -webkit-border-radius: 1px;
            -webkit-box-sizing: border-box;
        }

        .currency input[type=text]:hover {
            border: 1px solid #b9b9b9;
            border-top: 1px solid #a0a0a0;
            box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
            -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,.1);
        }

        .currency input[type=text]:focus {
            border: 1px solid #4d90fe;
            box-shadow: inset 0 1px 2px rgba(0,0,0,.3);
            outline: 0;
            -webkit-box-shadow: inset 0 1px 2px rgba(0,0,0,.3);
        }

        .z1asCe svg {
            display: block;
            height: 100%;
            width: 100%;
        }

        @-webkit-keyframes allow-alert {
            from {
                opacity: 1;
            }

            to {
                opacity: .35;
            }
        }

        .iUh30 {
            font-size: 14px;
            padding-top: 1px;
            line-height: 1.43;
        }

        .f a:link {
            color: #777;
        }

        #nygTcd>i,.a,.bc a:link,cite,cite a:link,cite a:visited {
            color: #006621;
            font-style: normal;
        }

        .fl a,.gl a:link,.mblink b,a.fl:link {
            color: #1a0dab;
        }

        #brs a:hover,#nav a.pn:hover,#nycp a:hover,#rcnt a:hover {
            text-decoration: underline;
        }

        #rcnt .ab_dropdownitem a:hover,#rcnt .kno-fb-ctx>a:hover,#rcnt [role=button]:hover,#rcnt a.a-no-hover-decoration:hover,#rcnt a.kpbb:hover {
            text-decoration: none;
        }

        .dPAwzb a {
            font-size: 18px;
            line-height: 1.33;
        }

        .rc {
            position: relative;
        }

        a:hover h3 {
            text-decoration: underline;
        }

        .r {
            font-size: small;
        }

        .r {
            line-height: 1.54;
        }

        .rc .s {
            line-height: 1.54;
        }

        .srg .g:last-of-type {
            margin-bottom: 28px;
        }

        #hdtb-more-mn a,.hdtb-mitem a {
            padding: 0 16px;
            color: #777;
            text-decoration: none;
            display: block;
        }

        .hdtb-mitem a {
            margin: 0 8px;
            padding: 0 8px;
        }

        #hdtb.notl a,#hdtb.notl div,#hdtb.notl li {
            outline-width: 0;
            outline: 0;
        }

        #hdtb .hdtb-mitem a:active {
            color: #1a73e8;
        }

        .hdtb-dd-mn a,.hdtb-dd-mn a:active,.hdtb-dd-mn a:visited {
            color: inherit;
            display: block;
            text-decoration: none;
        }

        #hdtb-more-mn a:hover,.hdtbItm a:hover {
            background-color: #f1f1f1;
        }

        #hdtb .hdtbItm a,#hdtb-more-mn a {
            color: #777;
            text-decoration: none;
            padding: 6px 44px 6px 30px;
            line-height: 17px;
            display: block;
        }

        .hdtb-mitem a {
            display: inline-block;
        }

        #hdtb-more-mn a {
            display: block;
            padding: 6px 16px;
            margin: 0;
        }

        #hdtb .hdtb-mitem a {
            color: #777;
        }

        .TbwUpd {
            display: inline-block;
        }

        .TbwUpd {
            line-height: 1.54;
        }

        .st sup {
            line-height: .9;
        }

        .mOd06 em {
            font-weight: 700!important;
        }

        .hdtbU li {
            list-style: none outside none;
        }

        #hdtb form {
            display: inline;
        }

        .vk_c a {
            text-decoration: none;
        }

        .vk_fl a {
            color: #878787;
        }

        .vk_fl a:hover {
            color: #1a0dab;
        }

        .di8g3 a:hover {
            text-decoration: underline;
        }

        .vk_tbl td {
            padding: 0;
        }

        a:hover h3.LC20lb {
            text-decoration: underline;
        }

        .LC20lb {
            display: inline-block;
            line-height: 1.33;
        }

        .TbwUpd {
            padding-bottom: 1px;
            padding-top: 1px;
        }

        .Lu0opc.eSq3C:hover g-fab {
            color: #222 !important;
        }

        .BlOseb.eSq3C g-fab,.k2Oeod.eSq3C g-fab {
            box-shadow: 0 0 0 1px rgba(0,0,0,0.04),0 4px 8px 0 rgba(0,0,0,0.20);
            cursor: pointer;
            height: 36px;
            width: 36px;
        }

        #brs .med {
            color: #222;
            height: auto;
            padding-bottom: 8px;
        }

        #brs a {
            padding: 3px 40px 3px 0;
            display: inline-block;
            float: left;
        }

        #brs a {
            text-decoration: none;
        }
    }
</style>