---
title: Метод Ибаккграундкопифиле Жетлокалнаме (Deliveryoptimization. h)
description: Возвращает локальное имя файла.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Метод Жетлокалнаме
- Метод Жетлокалнаме, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Жетлокалнаме
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071539"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>Метод Ибаккграундкопифиле:: Жетлокалнаме

Возвращает локальное имя файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппнаме* \[ заполняет\]
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая имя файла на клиенте. Полное имя. Вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить *ппнаме* по завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопифиле**](ibackgroundcopyfile.md)
</dt> <dt>

[**Ибаккграундкопифиле:: Жетремотенаме**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

