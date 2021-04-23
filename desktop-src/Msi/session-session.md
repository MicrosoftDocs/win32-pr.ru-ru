---
description: Свойство Property объекта Session является свойством для чтения и записи, представляющим строковое значение именованного свойства установщика, которое поддерживается объектом Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Свойство Session. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679940"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="5a55d-103">Свойство Session. Property</span><span class="sxs-lookup"><span data-stu-id="5a55d-103">Session.Property property</span></span>

<span data-ttu-id="5a55d-104">Свойство **Property** объекта [**Session**](session-object.md) — это свойство, доступное для чтения и записи, которое представляет строковое значение именованного свойства установщика, которое поддерживается объектом **Session** в таблице свойств в памяти, или значение, если в качестве префикса используется знак процента (%), значением системной переменной среды для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="5a55d-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="5a55d-105">Может быть указано либо строковое, либо целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="5a55d-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="5a55d-106">Несуществующее свойство или переменная среды эквивалентны ее значению NULL.</span><span class="sxs-lookup"><span data-stu-id="5a55d-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="5a55d-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5a55d-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a55d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a55d-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5a55d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a55d-109">Property value</span></span>

<span data-ttu-id="5a55d-110">Обязательное имя свойства с учетом регистра или имя переменной среды без учета регистра с префиксом процента (%).</span><span class="sxs-lookup"><span data-stu-id="5a55d-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a55d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5a55d-111">Requirements</span></span>



| <span data-ttu-id="5a55d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="5a55d-112">Requirement</span></span> | <span data-ttu-id="5a55d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="5a55d-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a55d-114">Версия</span><span class="sxs-lookup"><span data-stu-id="5a55d-114">Version</span></span><br/> | <span data-ttu-id="5a55d-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5a55d-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5a55d-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a55d-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5a55d-117">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a55d-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5a55d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5a55d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a55d-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a55d-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5a55d-120">IID</span><span class="sxs-lookup"><span data-stu-id="5a55d-120">IID</span></span><br/>     | <span data-ttu-id="5a55d-121">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5a55d-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




