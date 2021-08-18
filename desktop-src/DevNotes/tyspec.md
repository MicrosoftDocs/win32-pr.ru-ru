---
description: Определяет способы сопоставления с ИДЕНТИФИКАТОРом класса.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Перечисление ТИСПЕК
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075758"
---
# <a name="tyspec-enumeration"></a>Перечисление ТИСПЕК

Определяет способы сопоставления с ИДЕНТИФИКАТОРом класса.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**ТИСПЕК \_ CLSID**
</dt> <dd>

ИДЕНТИФИКАТОР CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**ТИСПЕК \_ филикст**
</dt> <dd>

Расширение имени файла. Это значение в настоящее время не поддерживается.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_тип MIME тиспек**
</dt> <dd>

Тип MIME. Это значение в настоящее время не поддерживается.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_имя файла тиспек**
</dt> <dd>

Имя файла. Это значение в настоящее время не поддерживается.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_идентификатор ProgID тиспек**
</dt> <dd>

ИДЕНТИФИКАТОР PROGID. Это значение в настоящее время не поддерживается.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**ТИСПЕК \_ PACKAGENAME**
</dt> <dd>

Имя пакета. Это значение в настоящее время не поддерживается.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID тиспек**
</dt> <dd>

Идентификатор объекта. Это значение в настоящее время не поддерживается.

</dd> </dl>

## <a name="remarks"></a>Remarks

Объединение **уклсспек** определяется следующим образом:

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Втипес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Соустановка**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
