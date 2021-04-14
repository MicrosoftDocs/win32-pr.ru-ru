---
title: IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize, свойство
description: Задает или получает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415173"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="c262f-112">Свойство IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize</span><span class="sxs-lookup"><span data-stu-id="c262f-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="c262f-113">Задает или получает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах).</span><span class="sxs-lookup"><span data-stu-id="c262f-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="c262f-114">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c262f-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c262f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c262f-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="c262f-116">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c262f-116">Property value</span></span>

<span data-ttu-id="c262f-117">Задает размер файла виртуального кэша для точечных рисунков 32 бит/с в мегабайтах (МБ).</span><span class="sxs-lookup"><span data-stu-id="c262f-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="c262f-118">Максимальное значение — 48 МБ.</span><span class="sxs-lookup"><span data-stu-id="c262f-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="c262f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c262f-119">Requirements</span></span>



| <span data-ttu-id="c262f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c262f-120">Requirement</span></span> | <span data-ttu-id="c262f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c262f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c262f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c262f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c262f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c262f-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c262f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c262f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c262f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c262f-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c262f-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c262f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="c262f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c262f-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c262f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c262f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c262f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c262f-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c262f-130">IID</span><span class="sxs-lookup"><span data-stu-id="c262f-130">IID</span></span><br/>                      | <span data-ttu-id="c262f-131">IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="c262f-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c262f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c262f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c262f-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c262f-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c262f-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c262f-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c262f-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c262f-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c262f-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c262f-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





