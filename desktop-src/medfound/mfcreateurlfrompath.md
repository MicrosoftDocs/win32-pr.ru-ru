---
description: Преобразует путь Microsoft MS-DOS в канонический URL-адрес.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Функция Мфкреатеурлфромпас
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739252"
---
# <a name="mfcreateurlfrompath-function"></a>Функция Мфкреатеурлфромпас

\[Этот API не поддерживается и может быть изменен или недоступен в будущем. Вместо этого приложения должны вызывать [урлкреатефромпас](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Преобразует путь Microsoft MS-DOS в канонический URL-адрес.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзфилепас* \[ в необязательное\]
</dt> <dd>

Строка, завершающаяся нулем, которая содержит путь. Максимальная длина строки — **\_ Максимальная \_ \_ Длина URL-адреса в Интернете**.

</dd> <dt>

*ппвсзфилеурл* \[ заполняет\]
</dt> <dd>

Получает строку, завершающуюся нулем, которая содержит URL-адрес. Вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                             | Описание                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Строка, заданная в параметре *пвсзфилепас* , уже имеет формат URL. В этом случае *псзфилепас* просто копируется в *ппсзфилеурл* без изменения.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>    | Функция выполнена успешно. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Remarks

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mfplat.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
