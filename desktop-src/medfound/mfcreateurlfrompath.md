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
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711276"
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



 

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mfplat.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
