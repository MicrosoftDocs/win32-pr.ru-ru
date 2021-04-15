---
description: Метод Саурцелистклеаралл объекта Patch очищает полный исходный список всех источников указанного типа для исправления. Принимает тип в качестве параметра. Этот метод вызывает Мсисаурцелистклеараллекс.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Метод PATCH. Саурцелистклеаралл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652033"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="4bd12-105">Метод PATCH. Саурцелистклеаралл</span><span class="sxs-lookup"><span data-stu-id="4bd12-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="4bd12-106">Метод **саурцелистклеаралл** объекта [**Patch**](patch-object.md) очищает полный исходный список всех источников указанного типа для исправления.</span><span class="sxs-lookup"><span data-stu-id="4bd12-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="4bd12-107">Принимает *тип* в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="4bd12-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="4bd12-108">Этот метод вызывает [**мсисаурцелистклеараллекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span><span class="sxs-lookup"><span data-stu-id="4bd12-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd12-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bd12-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="4bd12-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bd12-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bd12-111">*Тип*</span><span class="sxs-lookup"><span data-stu-id="4bd12-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="4bd12-112">Тип источника, например "сеть", "URL-адрес" или "носитель".</span><span class="sxs-lookup"><span data-stu-id="4bd12-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bd12-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bd12-113">Return value</span></span>

<span data-ttu-id="4bd12-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4bd12-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd12-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4bd12-115">Requirements</span></span>



| <span data-ttu-id="4bd12-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4bd12-116">Requirement</span></span> | <span data-ttu-id="4bd12-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4bd12-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd12-118">Версия</span><span class="sxs-lookup"><span data-stu-id="4bd12-118">Version</span></span><br/> | <span data-ttu-id="4bd12-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4bd12-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4bd12-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4bd12-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4bd12-121">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4bd12-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="4bd12-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4bd12-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="4bd12-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bd12-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="4bd12-124">IID</span><span class="sxs-lookup"><span data-stu-id="4bd12-124">IID</span></span><br/>     | <span data-ttu-id="4bd12-125">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4bd12-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="4bd12-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bd12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd12-127">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="4bd12-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="4bd12-128">**мсисаурцелистклеараллекс**</span><span class="sxs-lookup"><span data-stu-id="4bd12-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="4bd12-129">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="4bd12-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




