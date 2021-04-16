---
description: Свойство State возвращает состояние установки данного экземпляра обновления.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Свойство patch. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652148"
---
# <a name="patchstate-property"></a><span data-ttu-id="9571f-103">Свойство patch. State</span><span class="sxs-lookup"><span data-stu-id="9571f-103">Patch.State property</span></span>

<span data-ttu-id="9571f-104">Свойство **State** возвращает состояние установки данного экземпляра обновления.</span><span class="sxs-lookup"><span data-stu-id="9571f-104">The **State** property returns the installation state of this instance of the patch.</span></span>

<span data-ttu-id="9571f-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9571f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9571f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9571f-106">Syntax</span></span>


```JScript
propVal = Patch.State
```



## <a name="property-value"></a><span data-ttu-id="9571f-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9571f-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9571f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9571f-108">Remarks</span></span>

<span data-ttu-id="9571f-109">Это свойство возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9571f-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="9571f-110">Состояние установки</span><span class="sxs-lookup"><span data-stu-id="9571f-110">Installation State</span></span>        | <span data-ttu-id="9571f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9571f-111">Meaning</span></span>                                                      |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="9571f-112">МСИПАТЧСТАТЕ \_ применено</span><span class="sxs-lookup"><span data-stu-id="9571f-112">MSIPATCHSTATE\_APPLIED</span></span>    | <span data-ttu-id="9571f-113">К этому экземпляру продукта применено исправление.</span><span class="sxs-lookup"><span data-stu-id="9571f-113">Patch is applied to this product instance.</span></span>                   |
| <span data-ttu-id="9571f-114">МСИПАТЧСТАТЕ \_ заменено</span><span class="sxs-lookup"><span data-stu-id="9571f-114">MSIPATCHSTATE\_SUPERSEDED</span></span> | <span data-ttu-id="9571f-115">Исправление применено к этому экземпляру продукта, но заменено.</span><span class="sxs-lookup"><span data-stu-id="9571f-115">Patch is applied to this product instance but is superseded.</span></span> |
| <span data-ttu-id="9571f-116">МСИПАТЧСТАТЕ \_ устарел</span><span class="sxs-lookup"><span data-stu-id="9571f-116">MSIPATCHSTATE\_OBSOLETED</span></span>  | <span data-ttu-id="9571f-117">Исправление установлено в этом экземпляре продукта, но устарело.</span><span class="sxs-lookup"><span data-stu-id="9571f-117">Patch is applied in this product instance but obsolete.</span></span>      |



 

<span data-ttu-id="9571f-118">Этот метод может возвращать ошибку \_ неизвестное \_ исправление, если объект [**Patch**](patch-object.md) инициализируется пустой строкой для *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="9571f-118">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9571f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9571f-119">Requirements</span></span>



| <span data-ttu-id="9571f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9571f-120">Requirement</span></span> | <span data-ttu-id="9571f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9571f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9571f-122">Версия</span><span class="sxs-lookup"><span data-stu-id="9571f-122">Version</span></span><br/> | <span data-ttu-id="9571f-123">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9571f-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9571f-124">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9571f-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9571f-125">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9571f-125">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9571f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9571f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9571f-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9571f-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9571f-128">IID</span><span class="sxs-lookup"><span data-stu-id="9571f-128">IID</span></span><br/>     | <span data-ttu-id="9571f-129">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9571f-129">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9571f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9571f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9571f-131">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="9571f-131">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="9571f-132">**мсижетпатчинфоекс**</span><span class="sxs-lookup"><span data-stu-id="9571f-132">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="9571f-133">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="9571f-133">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




