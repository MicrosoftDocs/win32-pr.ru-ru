---
description: Свойство FieldCount объекта Record является свойством, предназначенным только для чтения и возвращающим количество полей в записи. Доступ для чтения к полям за пределами этого количества возвращает значения NULL. Ошибка доступа для записи.
ms.assetid: 50be848a-2d38-4768-aeb4-25cbaedade01
title: Свойство Record. FieldCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FieldCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 548c1da4c2a0106cbcd667b5ce3c915ec17bf1ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675646"
---
# <a name="recordfieldcount-property"></a><span data-ttu-id="ca250-105">Свойство Record. FieldCount</span><span class="sxs-lookup"><span data-stu-id="ca250-105">Record.FieldCount property</span></span>

<span data-ttu-id="ca250-106">Свойство **FieldCount** объекта [**Record**](record-object.md) является свойством, предназначенным только для чтения и возвращающим количество полей в записи.</span><span class="sxs-lookup"><span data-stu-id="ca250-106">The **FieldCount** property of the [**Record**](record-object.md) object is a read-only property that returns the number of fields in the record.</span></span> <span data-ttu-id="ca250-107">Доступ для чтения к полям за пределами этого количества возвращает значения NULL.</span><span class="sxs-lookup"><span data-stu-id="ca250-107">Read access to fields beyond this count returns Null values.</span></span> <span data-ttu-id="ca250-108">Ошибка доступа для записи.</span><span class="sxs-lookup"><span data-stu-id="ca250-108">Write access fails.</span></span>

<span data-ttu-id="ca250-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ca250-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca250-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca250-110">Syntax</span></span>


```JScript
propVal = Record.FieldCount
```



## <a name="property-value"></a><span data-ttu-id="ca250-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ca250-111">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ca250-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ca250-112">Requirements</span></span>



| <span data-ttu-id="ca250-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ca250-113">Requirement</span></span> | <span data-ttu-id="ca250-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ca250-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca250-115">Версия</span><span class="sxs-lookup"><span data-stu-id="ca250-115">Version</span></span><br/> | <span data-ttu-id="ca250-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca250-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca250-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca250-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca250-118">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca250-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ca250-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ca250-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca250-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca250-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ca250-121">IID</span><span class="sxs-lookup"><span data-stu-id="ca250-121">IID</span></span><br/>     | <span data-ttu-id="ca250-122">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ca250-122">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




