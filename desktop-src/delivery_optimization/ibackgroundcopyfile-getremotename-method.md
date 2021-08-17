---
title: Метод Ибаккграундкопифиле Жетремотенаме (Deliveryoptimization. h)
description: Извлекает удаленное имя файла.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Метод Жетремотенаме
- Метод Жетремотенаме, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Жетремотенаме
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810337"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>Метод Ибаккграундкопифиле:: Жетремотенаме

Извлекает удаленное имя файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппнаме* \[ заполняет\]
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая удаленное имя переносимого файла. Полное имя. Вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить *ппнаме* по завершении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.

## <a name="remarks"></a>Remarks

Чтобы изменить имя удаленного файла, вызовите метод [**IBackgroundCopyFile2:: сетремотенаме**](ibackgroundcopyfile2-setremotename-method.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкопифиле**](ibackgroundcopyfile.md)
</dt> <dt>

[**Ибаккграундкопифиле:: Жетлокалнаме**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

