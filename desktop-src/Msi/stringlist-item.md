---
description: Свойство Item является свойством, предназначенным только для чтения и возвращающим строку в коллекции объектов Стринглист.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Стринглист. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652105"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="39836-103">Стринглист. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="39836-103">StringList.Item property</span></span>

<span data-ttu-id="39836-104">Свойство **Item** является свойством, предназначенным только для чтения и возвращающим строку в коллекции [**объектов стринглист**](stringlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="39836-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="39836-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="39836-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="39836-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39836-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="39836-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="39836-107">Property value</span></span>

<span data-ttu-id="39836-108">Номер индекса элемента с коллекцией строк.</span><span class="sxs-lookup"><span data-stu-id="39836-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="39836-109">Этот параметр обязателен.</span><span class="sxs-lookup"><span data-stu-id="39836-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="39836-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39836-110">Remarks</span></span>

<span data-ttu-id="39836-111">Клиент должен убедиться, что [**объект стринглист**](stringlist-object.md) существует и не пуст, прежде чем ссылаться на свойство **Item** .</span><span class="sxs-lookup"><span data-stu-id="39836-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="39836-112">Требования</span><span class="sxs-lookup"><span data-stu-id="39836-112">Requirements</span></span>



| <span data-ttu-id="39836-113">Требование</span><span class="sxs-lookup"><span data-stu-id="39836-113">Requirement</span></span> | <span data-ttu-id="39836-114">Значение</span><span class="sxs-lookup"><span data-stu-id="39836-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39836-115">Версия</span><span class="sxs-lookup"><span data-stu-id="39836-115">Version</span></span><br/> | <span data-ttu-id="39836-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="39836-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="39836-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="39836-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="39836-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="39836-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="39836-119">DLL</span><span class="sxs-lookup"><span data-stu-id="39836-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="39836-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39836-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="39836-121">IID</span><span class="sxs-lookup"><span data-stu-id="39836-121">IID</span></span><br/>     | <span data-ttu-id="39836-122">IID \_ истринглист определен как 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="39836-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




