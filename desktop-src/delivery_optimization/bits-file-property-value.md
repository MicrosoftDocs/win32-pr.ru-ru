---
title: Структура BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: BITS_FILE_PROPERTY_VALUE Union предоставляет значение свойства файла DO, основанное на значении из перечисления BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Структура BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710455"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="6700e-104">Структура BITS_FILE_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="6700e-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="6700e-105">**BITS_FILE_PROPERTY_VALUE** Union предоставляет значение свойства файла Do, основанное на значении из перечисления [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .</span><span class="sxs-lookup"><span data-stu-id="6700e-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="6700e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6700e-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="6700e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6700e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6700e-108">**String**</span><span class="sxs-lookup"><span data-stu-id="6700e-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="6700e-109">Это значение используется при использовании значения перечисления идентификатора свойства **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span><span class="sxs-lookup"><span data-stu-id="6700e-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6700e-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6700e-110">Requirements</span></span>



| <span data-ttu-id="6700e-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6700e-111">Requirement</span></span> | <span data-ttu-id="6700e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6700e-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6700e-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6700e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6700e-114">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6700e-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6700e-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6700e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6700e-116">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="6700e-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6700e-117">Header</span><span class="sxs-lookup"><span data-stu-id="6700e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6700e-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6700e-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6700e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6700e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6700e-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="6700e-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="6700e-121">**IBackgroundCopyFile5., свойство**</span><span class="sxs-lookup"><span data-stu-id="6700e-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="6700e-122">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="6700e-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





