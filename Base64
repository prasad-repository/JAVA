public static String binary(String imageurl) {
		String body = "";
		try {
			CloseableHttpClient httpClient = HttpClients.createDefault();

			HttpGet httpGet = new HttpGet(imageurl);

			try {
				CloseableHttpResponse httpResponse = httpClient.execute(httpGet);

				int code = httpResponse.getStatusLine().getStatusCode();

				ByteArrayOutputStream byteArrayOutputStream = new ByteArrayOutputStream();
				httpResponse.getEntity().writeTo(byteArrayOutputStream);

				body = Base64.getEncoder().encodeToString(byteArrayOutputStream.toByteArray());

			} catch (Exception e) {
				e.printStackTrace();
				System.out.println("Error " + e.getMessage());
			}

		} catch (Exception e) {
			e.printStackTrace();
			System.out.println("Error " + e.getMessage());

		}

		return body;
	}
