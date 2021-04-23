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
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647935"
---
# <a name="tyspec-enumeration"></a><span data-ttu-id="ad350-103">Перечисление ТИСПЕК</span><span class="sxs-lookup"><span data-stu-id="ad350-103">TYSPEC enumeration</span></span>

<span data-ttu-id="ad350-104">Определяет способы сопоставления с ИДЕНТИФИКАТОРом класса.</span><span class="sxs-lookup"><span data-stu-id="ad350-104">Defines ways of mapping to a class ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad350-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad350-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="ad350-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ad350-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ad350-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**ТИСПЕК \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="ad350-107"><span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC\_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-108">ИДЕНТИФИКАТОР CLSID.</span><span class="sxs-lookup"><span data-stu-id="ad350-108">A CLSID.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**ТИСПЕК \_ филикст**</span><span class="sxs-lookup"><span data-stu-id="ad350-109"><span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC\_FILEEXT**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-110">Расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="ad350-110">A file name extension.</span></span> <span data-ttu-id="ad350-111">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-111">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**\_тип MIME тиспек**</span><span class="sxs-lookup"><span data-stu-id="ad350-112"><span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC\_MIMETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-113">Тип MIME.</span><span class="sxs-lookup"><span data-stu-id="ad350-113">A MIME type.</span></span> <span data-ttu-id="ad350-114">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-114">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**\_имя файла тиспек**</span><span class="sxs-lookup"><span data-stu-id="ad350-115"><span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC\_FILENAME**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-116">Имя файла.</span><span class="sxs-lookup"><span data-stu-id="ad350-116">A file name.</span></span> <span data-ttu-id="ad350-117">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-117">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**\_идентификатор ProgID тиспек**</span><span class="sxs-lookup"><span data-stu-id="ad350-118"><span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC\_PROGID**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-119">ИДЕНТИФИКАТОР PROGID.</span><span class="sxs-lookup"><span data-stu-id="ad350-119">A PROGID.</span></span> <span data-ttu-id="ad350-120">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-120">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**ТИСПЕК \_ PACKAGENAME**</span><span class="sxs-lookup"><span data-stu-id="ad350-121"><span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC\_PACKAGENAME**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-122">Имя пакета.</span><span class="sxs-lookup"><span data-stu-id="ad350-122">A package name.</span></span> <span data-ttu-id="ad350-123">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-123">This value is not currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad350-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**\_ObjectID тиспек**</span><span class="sxs-lookup"><span data-stu-id="ad350-124"><span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC\_OBJECTID**</span></span>
</dt> <dd>

<span data-ttu-id="ad350-125">Идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="ad350-125">An object ID.</span></span> <span data-ttu-id="ad350-126">Это значение в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad350-126">This value is not currently supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad350-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad350-127">Remarks</span></span>

<span data-ttu-id="ad350-128">Объединение **уклсспек** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad350-128">The **uCLSSPEC** union is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="ad350-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ad350-129">Requirements</span></span>



| <span data-ttu-id="ad350-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ad350-130">Requirement</span></span> | <span data-ttu-id="ad350-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ad350-131">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad350-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ad350-132">IDL</span></span><br/> | <dl> <span data-ttu-id="ad350-133"><dt>Втипес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad350-133"><dt>Wtypes.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad350-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad350-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad350-135">**Соустановка**</span><span class="sxs-lookup"><span data-stu-id="ad350-135">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
