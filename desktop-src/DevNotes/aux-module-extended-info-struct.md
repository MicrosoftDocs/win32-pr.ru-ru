---
description: Содержит расширенные сведения о модуле.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Структура AUX_MODULE_EXTENDED_INFO (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648984"
---
# <a name="aux_module_extended_info-structure"></a><span data-ttu-id="e966f-103">\_ \_ Расширенная \_ информационная структура модуля AUX</span><span class="sxs-lookup"><span data-stu-id="e966f-103">AUX\_MODULE\_EXTENDED\_INFO structure</span></span>

<span data-ttu-id="e966f-104">Содержит расширенные сведения о модуле.</span><span class="sxs-lookup"><span data-stu-id="e966f-104">Contains extended module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e966f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e966f-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a><span data-ttu-id="e966f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e966f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e966f-107">**басиЦинфо**</span><span class="sxs-lookup"><span data-stu-id="e966f-107">**BasicInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e966f-108">[**\_ \_ Базовая \_ информационная структура модуля AUX**](aux-module-basic-info-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="e966f-108">An [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e966f-109">**ImageSize**</span><span class="sxs-lookup"><span data-stu-id="e966f-109">**ImageSize**</span></span>
</dt> <dd>

<span data-ttu-id="e966f-110">Размер загруженного модуля в байтах.</span><span class="sxs-lookup"><span data-stu-id="e966f-110">The size, in bytes, of the loaded module.</span></span>

</dd> <dt>

<span data-ttu-id="e966f-111">**филенамеоффсет**</span><span class="sxs-lookup"><span data-stu-id="e966f-111">**FileNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e966f-112">Смещение имени файла в буфере **фуллпаснаме** .</span><span class="sxs-lookup"><span data-stu-id="e966f-112">The offset of the file name within the **FullPathName** buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e966f-113">**фуллпаснаме**</span><span class="sxs-lookup"><span data-stu-id="e966f-113">**FullPathName**</span></span>
</dt> <dd>

<span data-ttu-id="e966f-114">Полный путь к модулю.</span><span class="sxs-lookup"><span data-stu-id="e966f-114">The full path of the module.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e966f-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e966f-115">Remarks</span></span>

<span data-ttu-id="e966f-116">Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="e966f-116">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="e966f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e966f-117">Requirements</span></span>



| <span data-ttu-id="e966f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e966f-118">Requirement</span></span> | <span data-ttu-id="e966f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e966f-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e966f-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e966f-120">Redistributable</span></span><br/> | <span data-ttu-id="e966f-121">Библиотека вспомогательных API Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e966f-121">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="e966f-122">Header</span><span class="sxs-lookup"><span data-stu-id="e966f-122">Header</span></span><br/>          | <dl> <span data-ttu-id="e966f-123"><dt>AUX \_ клиб. h</dt></span><span class="sxs-lookup"><span data-stu-id="e966f-123"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e966f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e966f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e966f-125">**ауксклибкуеримодулеинформатион**</span><span class="sxs-lookup"><span data-stu-id="e966f-125">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[<span data-ttu-id="e966f-126">**\_ \_ основные \_ сведения о модуле AUX**</span><span class="sxs-lookup"><span data-stu-id="e966f-126">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




