---
description: Метод Fetch объекта View возвращает следующую строку данных столбца, если в результирующем наборе доступно больше строк, в противном случае — значение null. Вызовите метод Execute перед методом FETCH.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: Метод представления. FETCH
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674887"
---
# <a name="viewfetch-method"></a><span data-ttu-id="892ad-104">Метод представления. FETCH</span><span class="sxs-lookup"><span data-stu-id="892ad-104">View.Fetch method</span></span>

<span data-ttu-id="892ad-105">Метод **Fetch** объекта [**View**](view-object.md) возвращает следующую строку данных столбца, если в результирующем наборе доступно больше строк, в противном случае — значение null.</span><span class="sxs-lookup"><span data-stu-id="892ad-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="892ad-106">Вызовите метод [**EXECUTE**](view-execute.md) перед методом **Fetch** .</span><span class="sxs-lookup"><span data-stu-id="892ad-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="892ad-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="892ad-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="892ad-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="892ad-108">Parameters</span></span>

<span data-ttu-id="892ad-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="892ad-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="892ad-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="892ad-110">Return value</span></span>

<span data-ttu-id="892ad-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="892ad-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="892ad-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="892ad-112">Remarks</span></span>

<span data-ttu-id="892ad-113">Один и тот же объект [**записи**](record-object.md) следует использовать для получения данных в нескольких строках, иначе объект должен быть освобожден путем выхода из области видимости.</span><span class="sxs-lookup"><span data-stu-id="892ad-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="892ad-114">Запись можно проверить на конец результирующего набора, используя синтаксис "If Фетчрекорд Nothing".</span><span class="sxs-lookup"><span data-stu-id="892ad-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="892ad-115">Требования</span><span class="sxs-lookup"><span data-stu-id="892ad-115">Requirements</span></span>



| <span data-ttu-id="892ad-116">Требование</span><span class="sxs-lookup"><span data-stu-id="892ad-116">Requirement</span></span> | <span data-ttu-id="892ad-117">Значение</span><span class="sxs-lookup"><span data-stu-id="892ad-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892ad-118">Версия</span><span class="sxs-lookup"><span data-stu-id="892ad-118">Version</span></span><br/> | <span data-ttu-id="892ad-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="892ad-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="892ad-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="892ad-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="892ad-121">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="892ad-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="892ad-122">DLL</span><span class="sxs-lookup"><span data-stu-id="892ad-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="892ad-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="892ad-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="892ad-124">IID</span><span class="sxs-lookup"><span data-stu-id="892ad-124">IID</span></span><br/>     | <span data-ttu-id="892ad-125">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="892ad-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




