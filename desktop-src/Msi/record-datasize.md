---
description: Свойство DataSize объекта Record является свойством, предназначенным только для чтения и возвращающим размер данных для указанного поля.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Свойство Record. DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651948"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="27690-103">Свойство Record. DataSize</span><span class="sxs-lookup"><span data-stu-id="27690-103">Record.DataSize property</span></span>

<span data-ttu-id="27690-104">Свойство **DataSize** объекта [**Record**](record-object.md) является свойством, предназначенным только для чтения и возвращающим размер данных для указанного поля.</span><span class="sxs-lookup"><span data-stu-id="27690-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="27690-105">Если данные являются потоком, возвращается длина потока в байтах.</span><span class="sxs-lookup"><span data-stu-id="27690-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="27690-106">Если данные являются строкой, то возвращается длина строки без значения NULL.</span><span class="sxs-lookup"><span data-stu-id="27690-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="27690-107">Если данные являются целым числом, возвращается значение 4 (что означает размер целого числа).</span><span class="sxs-lookup"><span data-stu-id="27690-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="27690-108">Если данные равны NULL, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="27690-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="27690-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="27690-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27690-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27690-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="27690-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="27690-111">Property value</span></span>

<span data-ttu-id="27690-112">Обязательный номер поля значения в записи, 1.</span><span class="sxs-lookup"><span data-stu-id="27690-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="27690-113">Требования</span><span class="sxs-lookup"><span data-stu-id="27690-113">Requirements</span></span>



| <span data-ttu-id="27690-114">Требование</span><span class="sxs-lookup"><span data-stu-id="27690-114">Requirement</span></span> | <span data-ttu-id="27690-115">Значение</span><span class="sxs-lookup"><span data-stu-id="27690-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27690-116">Версия</span><span class="sxs-lookup"><span data-stu-id="27690-116">Version</span></span><br/> | <span data-ttu-id="27690-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="27690-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="27690-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="27690-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="27690-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="27690-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="27690-120">DLL</span><span class="sxs-lookup"><span data-stu-id="27690-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="27690-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27690-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="27690-122">IID</span><span class="sxs-lookup"><span data-stu-id="27690-122">IID</span></span><br/>     | <span data-ttu-id="27690-123">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="27690-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




