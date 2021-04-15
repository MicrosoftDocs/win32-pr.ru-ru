---
description: Метод PERSISTED объекта Суммаринфо форматирует и записывает ранее сохраненные свойства в стандартный поток SummaryInformation.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Суммаринфо. PERSISTED, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675747"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="f377a-103">Суммаринфо. PERSISTED, метод</span><span class="sxs-lookup"><span data-stu-id="f377a-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="f377a-104">Метод **PERSISTED** объекта [**суммаринфо**](summaryinfo-object.md) форматирует и записывает ранее сохраненные свойства в стандартный поток SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="f377a-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="f377a-105">Он выдает ошибку, если поток не может быть успешно записан.</span><span class="sxs-lookup"><span data-stu-id="f377a-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="f377a-106">Этот метод может вызываться только один раз после задания всех значений свойств.</span><span class="sxs-lookup"><span data-stu-id="f377a-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="f377a-107">Свойства по-прежнему могут быть считаны после того, как поток записывается.</span><span class="sxs-lookup"><span data-stu-id="f377a-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="f377a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f377a-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="f377a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f377a-109">Parameters</span></span>

<span data-ttu-id="f377a-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f377a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f377a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f377a-111">Return value</span></span>

<span data-ttu-id="f377a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f377a-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f377a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f377a-113">Requirements</span></span>



| <span data-ttu-id="f377a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f377a-114">Requirement</span></span> | <span data-ttu-id="f377a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f377a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f377a-116">Версия</span><span class="sxs-lookup"><span data-stu-id="f377a-116">Version</span></span><br/> | <span data-ttu-id="f377a-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f377a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f377a-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f377a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f377a-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="f377a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f377a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f377a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f377a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f377a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f377a-122">IID</span><span class="sxs-lookup"><span data-stu-id="f377a-122">IID</span></span><br/>     | <span data-ttu-id="f377a-123">IID \_ исуммаринфо определяется как 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f377a-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




