---
description: выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий файл .cab.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'Метод Иеаксисервицекаллбакк:: Верифифиле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3c8072680d42e214304cae1f0a6002b7a1fbc036fc075c5c6777dd7612733a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414714"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Метод Иеаксисервицекаллбакк:: Верифифиле

метод **верифифиле** выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий файл .cab.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрфилеурл* \[ окне\]
</dt> <dd>

URL-адрес объекта ActiveX для проверки.

</dd> <dt>

*бстраппроведфиленаме* \[ заполняет\]
</dt> <dd>

имя файла, в который был скачан файл .cab, связанный с объектом ActiveX.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Business, Windows vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервицекаллбакк определен как 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иеаксисервицекаллбакк**](ieaxiservicecallback.md)
</dt> </dl>

 

