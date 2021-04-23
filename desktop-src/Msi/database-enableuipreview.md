---
description: Метод Енаблеуипревиев объекта Database упрощает создание диалоговых окон и объявлений, предоставляя поддержку, необходимую для просмотра диалоговых окон пользовательского интерфейса, хранящихся в базе данных установщика.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Database. Енаблеуипревиев, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669122"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="310b4-103">Database. Енаблеуипревиев, метод</span><span class="sxs-lookup"><span data-stu-id="310b4-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="310b4-104">Метод **енаблеуипревиев** объекта [**Database**](database-object.md) упрощает создание диалоговых окон и объявлений, предоставляя поддержку, необходимую для просмотра диалоговых окон пользовательского интерфейса, хранящихся в базе данных установщика.</span><span class="sxs-lookup"><span data-stu-id="310b4-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="310b4-105">Метод запускает режим предварительного просмотра, возвращая предварительный объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="310b4-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="310b4-106">Режим предварительного просмотра заканчивается при освобождении объекта предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="310b4-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="310b4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="310b4-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="310b4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="310b4-108">Parameters</span></span>

<span data-ttu-id="310b4-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="310b4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="310b4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="310b4-110">Return value</span></span>

<span data-ttu-id="310b4-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="310b4-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="310b4-112">Требования</span><span class="sxs-lookup"><span data-stu-id="310b4-112">Requirements</span></span>



| <span data-ttu-id="310b4-113">Требование</span><span class="sxs-lookup"><span data-stu-id="310b4-113">Requirement</span></span> | <span data-ttu-id="310b4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="310b4-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310b4-115">Версия</span><span class="sxs-lookup"><span data-stu-id="310b4-115">Version</span></span><br/> | <span data-ttu-id="310b4-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="310b4-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="310b4-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="310b4-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="310b4-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="310b4-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="310b4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="310b4-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="310b4-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="310b4-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="310b4-121">IID</span><span class="sxs-lookup"><span data-stu-id="310b4-121">IID</span></span><br/>     | <span data-ttu-id="310b4-122">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="310b4-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




