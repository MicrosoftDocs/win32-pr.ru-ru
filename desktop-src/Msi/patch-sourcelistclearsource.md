---
description: Удаляет сетевой источник или URL-адрес.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Метод PATCH. Саурцелистклеарсаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651708"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="0c928-103">Метод PATCH. Саурцелистклеарсаурце</span><span class="sxs-lookup"><span data-stu-id="0c928-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="0c928-104">Метод **саурцелистклеарсаурце** удаляет сеть или источник URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="0c928-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="0c928-105">Этот метод вызывает [**мсисаурцелистклеарсаурце**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="0c928-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c928-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c928-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="0c928-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c928-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c928-108">*Тип*</span><span class="sxs-lookup"><span data-stu-id="0c928-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="0c928-109">Тип удаляемого источника.</span><span class="sxs-lookup"><span data-stu-id="0c928-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="0c928-110">**МСИСАУРЦЕТИПЕ \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="0c928-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="0c928-111">**\_URL-адрес мсисаурцетипе**</span><span class="sxs-lookup"><span data-stu-id="0c928-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0c928-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="0c928-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0c928-113">Путь к удаляемому источнику.</span><span class="sxs-lookup"><span data-stu-id="0c928-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c928-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c928-114">Return value</span></span>

<span data-ttu-id="0c928-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0c928-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c928-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0c928-116">Requirements</span></span>



| <span data-ttu-id="0c928-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0c928-117">Requirement</span></span> | <span data-ttu-id="0c928-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0c928-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c928-119">Версия</span><span class="sxs-lookup"><span data-stu-id="0c928-119">Version</span></span><br/> | <span data-ttu-id="0c928-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c928-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c928-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c928-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c928-122">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0c928-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0c928-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0c928-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c928-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c928-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0c928-125">IID</span><span class="sxs-lookup"><span data-stu-id="0c928-125">IID</span></span><br/>     | <span data-ttu-id="0c928-126">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0c928-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0c928-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c928-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c928-128">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="0c928-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0c928-129">**мсисаурцелистклеарсаурце**</span><span class="sxs-lookup"><span data-stu-id="0c928-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="0c928-130">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="0c928-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




