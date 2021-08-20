---
description: Извлекает основные атрибуты для указанного файлового объекта.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Функция Нткуеряттрибутесфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: e6b1ecdc7cc7f0a5c18afc3eeb613c3f9cd9a38aa22a876ad156c3d1c6b1bc97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826810"
---
# <a name="ntqueryattributesfile-function"></a>Функция Нткуеряттрибутесфиле

\[эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]

Извлекает основные атрибуты для указанного файлового объекта.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Обжектаттрибутес* \[ окне\]
</dt> <dd>

Указатель на структуру [ \_ атрибутов объекта](https://msdn.microsoft.com/library/aa491657.aspx) , которая предоставляет атрибуты, используемые для файлового объекта.

</dd> <dt>

*Филеинформатион* \[ заполняет\]
</dt> <dd>

Указатель на [ \_ \_ информационную структуру файла Basic](https://msdn.microsoft.com/library/aa491634.aspx) для получения возвращаемых сведений об атрибутах файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает код NTSTATUS или ошибки.

Формы и значения кодов ошибок NTSTATUS перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.

## <a name="remarks"></a>Remarks

Эта функция не имеет связанного файла заголовка. Связанная библиотека импорта, NTDLL. lib, доступна в WDK. Можно также использовать функции [**LoadLibrary**](-loadlibrary.md) и [**GetProcAddress**](-getprocaddress-.md) для динамической привязки к Ntdll.dll.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




