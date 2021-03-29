---
description: Добавляет строку и дополнительные данные в таблицу.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: Функция Псетупстрингтаблеаддстринжекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665412"
---
# <a name="psetupstringtableaddstringex-function"></a>Функция Псетупстрингтаблеаддстринжекс

\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]

Добавляет строку и дополнительные данные в таблицу.

## <a name="syntax"></a>Синтаксис


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*STRINGTABLE* \[ окне\]
</dt> <dd>

Указатель на таблицу строк.

</dd> <dt>

*Строка* \[ окне\]
</dt> <dd>

Указатель на строку, добавляемую в таблицу.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Значение этого параметра может быть равно `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Значение                                                                                                                                                                                                                                             | Значение                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**Стртаб \_ 0x001 \_ с учетом регистра**</dt> <dt></dt> </dl> | В строке учитывается регистр.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**Стртаб \_ НОВЫЙ \_ екстрадата**</dt> <dt>0x004</dt> </dl>    | Имеются дополнительные данные.<br/>      |



 

</dd> <dt>

*Екстрадата* \[ в необязательное\]
</dt> <dd>

Необязательный указатель на дополнительный объект данных.

</dd> <dt>

*Екстрадатасизе* \[ в необязательное\]
</dt> <dd>

Размер дополнительных данных.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
