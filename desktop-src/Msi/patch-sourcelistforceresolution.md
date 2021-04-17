---
description: Метод Саурцелистфорцересолутион очищает последнее использованное свойство Source.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Метод PATCH. Саурцелистфорцересолутион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651707"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="764c3-103">Метод PATCH. Саурцелистфорцересолутион</span><span class="sxs-lookup"><span data-stu-id="764c3-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="764c3-104">Метод **саурцелистфорцересолутион** очищает последнее использованное свойство Source.</span><span class="sxs-lookup"><span data-stu-id="764c3-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="764c3-105">При этом установщик будет выполнять поиск допустимого источника исправления в списке источников, если в следующий раз требуется источник исправления.</span><span class="sxs-lookup"><span data-stu-id="764c3-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="764c3-106">Например, установщик требует, чтобы источник обновления выполнил установку или переустановку, если отсутствует копия локального кэша обновления.</span><span class="sxs-lookup"><span data-stu-id="764c3-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="764c3-107">Этот метод вызывает [**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="764c3-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="764c3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="764c3-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="764c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="764c3-109">Parameters</span></span>

<span data-ttu-id="764c3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="764c3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="764c3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="764c3-111">Return value</span></span>

<span data-ttu-id="764c3-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="764c3-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="764c3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="764c3-113">Requirements</span></span>



| <span data-ttu-id="764c3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="764c3-114">Requirement</span></span> | <span data-ttu-id="764c3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="764c3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="764c3-116">Версия</span><span class="sxs-lookup"><span data-stu-id="764c3-116">Version</span></span><br/> | <span data-ttu-id="764c3-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="764c3-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="764c3-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="764c3-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="764c3-119">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="764c3-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="764c3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="764c3-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="764c3-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="764c3-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="764c3-122">IID</span><span class="sxs-lookup"><span data-stu-id="764c3-122">IID</span></span><br/>     | <span data-ttu-id="764c3-123">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="764c3-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="764c3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="764c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764c3-125">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="764c3-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="764c3-126">**мсисаурцелистфорцересолутион**</span><span class="sxs-lookup"><span data-stu-id="764c3-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="764c3-127">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="764c3-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




