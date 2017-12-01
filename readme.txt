111111
222222
33333


app=A001&cbi=1725&ct=1511754361203&fee=1&pt=1511754310000&sdk=0001&ssid=1366485446275629057&st=1&tcd=IWD11993070000001310610901994&uid=1199307&ver=1ZmY4MDgwODE1ZjViNmMwMTAxNWY3NzA3YzcxYTAxOGQ=

sign=3064613061376538333566366334633334613937393766376630626439353265, uid=1199307, fee=1, app=A001, pt=1511754310000, ssid=1366485446275629057, ver=1, st=1, sdk=0001, tcd=IWD11993070000001310610901994, cbi=1725, ct=1511754361203

ZmY4MDgwODE1ZjViNmMwMTAxNWY3NzA3YzcxYTAxOGQ=

1ZmY4MDgwODE1ZjViNmMwMTAxNWY3NzA3YzcxYTAxOGQ=


public static void main(String[] args) {
		
		Map<String, Object> requestParams = new HashMap<String, Object>();
		requestParams.put("app","A001");
		requestParams.put("cbi",1725);
		requestParams.put("ct","1511754361203");
		requestParams.put("fee",1);
		requestParams.put("pt","1511754310000");
		requestParams.put("sdk","0001");
		requestParams.put("ssid","1366485446275629057");
		requestParams.put("st",1);
		requestParams.put("tcd","IWD11993070000001310610901994");
		requestParams.put("uid","1199307");
		requestParams.put("ver","1");
		
		// »ñÈ¡´ýÇ©Ãû×Ö·û´®
		String preSignStr = AlipayCore.createLinkString2(requestParams);
		System.out.println(preSignStr);
		String getMD5Code = MD5.GetMD5Code(preSignStr+"ZmY4MDgwODE1ZjViNmMwMTAxNWY3NzA3YzcxYTAxOGQ=");
		System.out.println(getMD5Code);
		String sign = PayUtil.getHexSting(MD5.GetMD5Code(preSignStr+"ZmY4MDgwODE1ZjViNmMwMTAxNWY3NzA3YzcxYTAxOGQ="));
		System.out.println(sign);
		
	}