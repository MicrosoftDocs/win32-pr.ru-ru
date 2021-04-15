---
description: Метод Саурцелистаддсаурце добавляет сетевой источник или URL-адрес. Принимает параметры SourcePath, Type и index в качестве параметров. Этот метод вызывает Мсисаурцелистаддсаурцеекс.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Метод PATCH. Саурцелистаддсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651837"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="b8cbf-105">Метод PATCH. Саурцелистаддсаурце</span><span class="sxs-lookup"><span data-stu-id="b8cbf-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="b8cbf-106">Метод **саурцелистаддсаурце** добавляет сетевой источник или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="b8cbf-107">Принимает параметры *SourcePath*, *Type* и *index* в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="b8cbf-108">Этот метод вызывает [**мсисаурцелистаддсаурцеекс**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span><span class="sxs-lookup"><span data-stu-id="b8cbf-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8cbf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8cbf-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="b8cbf-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8cbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8cbf-111">*Тип*</span><span class="sxs-lookup"><span data-stu-id="b8cbf-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="b8cbf-112">Тип добавляемого источника: МСИСАУРЦЕТИПЕ \_ Network или мсисаурцетипе \_ URL.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="b8cbf-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="b8cbf-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="b8cbf-114">Путь к добавляемому источнику.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="b8cbf-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="b8cbf-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="b8cbf-116">Если **саурцелистаддсаурце** вызывается с новым источником и *индексом* , равным 0, установщик добавляет источник в конец исходного списка.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="b8cbf-117">Если эта функция вызывается с источником, уже существующим в списке источника, а *индекс* имеет значение 0, установщик оставляет существующий индекс источника.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="b8cbf-118">Если функция вызывается с существующим источником в исходном списке, а *индекс* имеет ненулевое значение, то источник удаляется из текущего расположения в списке и вставляется в позицию, указанную по *индексу*, перед любым источником, который уже существует в этой позиции.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="b8cbf-119">Если функция вызывается с новым источником, а для *индекса* задано ненулевое значение, то источник вставляется в позиции, указанной в параметре *index*, перед тем, как источник, который уже существует в этой позиции.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="b8cbf-120">Значение индекса для всех источников в списке после индекса, указанного в *индексе* , обновится, чтобы гарантировать уникальность значений индекса, а также гарантировать, что существующий порядок будет оставаться неизменным.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="b8cbf-121">Если *индекс* больше числа источников в списке, то источник помещается в конец списка, где значение индекса больше, чем у существующего источника.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8cbf-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8cbf-122">Return value</span></span>

<span data-ttu-id="b8cbf-123">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8cbf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b8cbf-124">Requirements</span></span>



| <span data-ttu-id="b8cbf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b8cbf-125">Requirement</span></span> | <span data-ttu-id="b8cbf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cbf-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8cbf-127">Версия</span><span class="sxs-lookup"><span data-stu-id="b8cbf-127">Version</span></span><br/> | <span data-ttu-id="b8cbf-128">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b8cbf-129">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b8cbf-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b8cbf-130">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b8cbf-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b8cbf-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b8cbf-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8cbf-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8cbf-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b8cbf-133">IID</span><span class="sxs-lookup"><span data-stu-id="b8cbf-133">IID</span></span><br/>     | <span data-ttu-id="b8cbf-134">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b8cbf-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b8cbf-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8cbf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cbf-136">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="b8cbf-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b8cbf-137">**мсисаурцелистаддсаурцеекс**</span><span class="sxs-lookup"><span data-stu-id="b8cbf-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="b8cbf-138">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="b8cbf-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




