---
description: Свойство Property объекта Уипревиев — это свойство, доступное для чтения и записи, которое представляет строковое значение именованного свойства установщика, или, если оно имеет префикс в виде знака процента (%), значение системной переменной среды для текущего процесса.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: Уипревиев. Property, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675461"
---
# <a name="uipreviewproperty-property"></a><span data-ttu-id="700d2-103">Уипревиев. Property, свойство</span><span class="sxs-lookup"><span data-stu-id="700d2-103">UIPreview.Property property</span></span>

<span data-ttu-id="700d2-104">Свойство **Property** объекта [**уипревиев**](uipreview-object.md) — это свойство, доступное для чтения и записи, которое представляет строковое значение именованного свойства установщика, или, если оно имеет префикс в виде знака процента (%), значение системной переменной среды для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="700d2-104">The **Property** property of the [**UIPreview**](uipreview-object.md) object is a read-write property that represents the string value of a named installer property, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="700d2-105">Это обеспечивает правильное отображение диалоговых окон, зависящих от значений свойств.</span><span class="sxs-lookup"><span data-stu-id="700d2-105">This is exposed to allow proper display of dialog boxes that are dependent upon property values.</span></span> <span data-ttu-id="700d2-106">Может быть указано либо строковое, либо целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="700d2-106">Either string or integer values may be supplied.</span></span> <span data-ttu-id="700d2-107">Несуществующее свойство или переменная среды эквивалентны ее значению NULL.</span><span class="sxs-lookup"><span data-stu-id="700d2-107">A nonexistent property or environment variable is equivalent to its value being null.</span></span>

<span data-ttu-id="700d2-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="700d2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="700d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="700d2-109">Syntax</span></span>


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="700d2-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="700d2-110">Property value</span></span>

<span data-ttu-id="700d2-111">Обязательное имя свойства с учетом регистра или имя переменной среды без учета регистра с префиксом процента (%).</span><span class="sxs-lookup"><span data-stu-id="700d2-111">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="700d2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="700d2-112">Requirements</span></span>



| <span data-ttu-id="700d2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="700d2-113">Requirement</span></span> | <span data-ttu-id="700d2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="700d2-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="700d2-115">Версия</span><span class="sxs-lookup"><span data-stu-id="700d2-115">Version</span></span><br/> | <span data-ttu-id="700d2-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="700d2-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="700d2-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="700d2-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="700d2-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="700d2-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="700d2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="700d2-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="700d2-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="700d2-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="700d2-121">IID</span><span class="sxs-lookup"><span data-stu-id="700d2-121">IID</span></span><br/>     | <span data-ttu-id="700d2-122">IID \_ иуипревиев определяется как 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="700d2-122">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




