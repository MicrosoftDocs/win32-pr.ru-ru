---
description: Свойство SummaryInformation объекта Database возвращает объект Суммаринфо, который может использоваться для проверки, обновления и добавления свойств в поток сводных данных.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Свойство Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652254"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="7eecf-103">Свойство Database. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="7eecf-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="7eecf-104">Свойство **SummaryInformation** объекта [**Database**](database-object.md) возвращает объект [**суммаринфо**](summaryinfo-object.md) , который может использоваться для проверки, обновления и добавления свойств в [поток сводных данных](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="7eecf-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="7eecf-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7eecf-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eecf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7eecf-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="7eecf-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7eecf-107">Property value</span></span>

<span data-ttu-id="7eecf-108">Максимальное число добавляемых или изменяемых свойств.</span><span class="sxs-lookup"><span data-stu-id="7eecf-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="7eecf-109">Этот параметр является обязательным и используется для выделения достаточной рабочей памяти во время создания потока.</span><span class="sxs-lookup"><span data-stu-id="7eecf-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="7eecf-110">Хранение этого количества свойств не требуется.</span><span class="sxs-lookup"><span data-stu-id="7eecf-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="7eecf-111">Значение, равное нулю, должно использоваться, если база данных открыта только для чтения, чтобы предотвратить обновление потока.</span><span class="sxs-lookup"><span data-stu-id="7eecf-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eecf-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7eecf-112">Remarks</span></span>

<span data-ttu-id="7eecf-113">Если для открытия существующего потока сводных данных используется значение *макспропертиес* больше 0, то перед закрытием объекта необходимо вызвать метод [**Persist**](summaryinfo-persist.md) .</span><span class="sxs-lookup"><span data-stu-id="7eecf-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="7eecf-114">В противном случае существующие сведения о потоке будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="7eecf-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="7eecf-115">Если свойство завершается неудачно, можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="7eecf-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eecf-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7eecf-116">Requirements</span></span>



| <span data-ttu-id="7eecf-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7eecf-117">Requirement</span></span> | <span data-ttu-id="7eecf-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7eecf-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eecf-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7eecf-119">Version</span></span><br/> | <span data-ttu-id="7eecf-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7eecf-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7eecf-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7eecf-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7eecf-122">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="7eecf-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7eecf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7eecf-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="7eecf-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7eecf-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7eecf-125">IID</span><span class="sxs-lookup"><span data-stu-id="7eecf-125">IID</span></span><br/>     | <span data-ttu-id="7eecf-126">IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7eecf-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




