---
description: Свойство Sources перечисляет все источники для экземпляра patch. Это свойство вызывает Мсисаурцелистенумсаурцес и возвращает массив строк и принимает тип источника в качестве аргумента.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Свойство patch. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651700"
---
# <a name="patchsources-property"></a><span data-ttu-id="7b775-104">Свойство patch. sources</span><span class="sxs-lookup"><span data-stu-id="7b775-104">Patch.Sources property</span></span>

<span data-ttu-id="7b775-105">Свойство **Sources** перечисляет все источники для экземпляра patch.</span><span class="sxs-lookup"><span data-stu-id="7b775-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="7b775-106">Это свойство вызывает [**мсисаурцелистенумсаурцес**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) и возвращает массив строк и принимает тип источника в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="7b775-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="7b775-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7b775-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b775-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b775-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="7b775-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7b775-109">Property value</span></span>

<span data-ttu-id="7b775-110">Тип источника для перечисления.</span><span class="sxs-lookup"><span data-stu-id="7b775-110">The type of source to enumerate.</span></span> <span data-ttu-id="7b775-111">Значение может быть *мсиинсталлсаурцетипенетворк* (1) или *мсиинсталлсаурцетипеурл* (2).</span><span class="sxs-lookup"><span data-stu-id="7b775-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b775-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7b775-112">Requirements</span></span>



| <span data-ttu-id="7b775-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7b775-113">Requirement</span></span> | <span data-ttu-id="7b775-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7b775-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b775-115">Версия</span><span class="sxs-lookup"><span data-stu-id="7b775-115">Version</span></span><br/> | <span data-ttu-id="7b775-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b775-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b775-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b775-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b775-118">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7b775-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="7b775-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7b775-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b775-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b775-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="7b775-121">IID</span><span class="sxs-lookup"><span data-stu-id="7b775-121">IID</span></span><br/>     | <span data-ttu-id="7b775-122">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7b775-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="7b775-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b775-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b775-124">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="7b775-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="7b775-125">**мсисаурцелистенумсаурцес**</span><span class="sxs-lookup"><span data-stu-id="7b775-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="7b775-126">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="7b775-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




