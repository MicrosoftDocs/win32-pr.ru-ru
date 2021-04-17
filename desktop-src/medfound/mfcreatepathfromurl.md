---
description: Преобразует URL-адрес файла в путь Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: Функция Мфкреатепасфромурл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711275"
---
# <a name="mfcreatepathfromurl-function"></a>Функция Мфкреатепасфромурл

\[Этот API не поддерживается и может быть изменен или недоступен в будущем. Вместо этого приложения должны вызывать [**паскреатефромурл**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]

Преобразует URL-адрес файла в путь Microsoft MS-DOS.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзфилеурл* \[ в необязательное\]
</dt> <dd>

Строка, завершающаяся нулем и содержащая URL-адрес. Максимальная длина строки — **\_ Максимальная \_ \_ Длина URL-адреса в Интернете**.

</dd> <dt>

*ппвсзфилепас* \[ заполняет\]
</dt> <dd>

Получает строку, завершающуюся нулем, которая содержит URL-адрес. Вызывающий объект должен освободить строку, вызвав [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Функция выполнена успешно. <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент. Строка, указанная в параметре *пвсзфилеурл* , не может быть преобразована в путь.<br/> |



 

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

 

 
