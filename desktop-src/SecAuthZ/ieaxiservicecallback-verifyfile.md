---
description: Выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.
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
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546530"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>Метод Иеаксисервицекаллбакк:: Верифифиле

Метод **верифифиле** выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.

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

Имя файла, в который был скачан CAB-файл, связанный с объектом ActiveX.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервицекаллбакк определен как 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иеаксисервицекаллбакк**](ieaxiservicecallback.md)
</dt> </dl>

 

