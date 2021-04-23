---
description: Метод Close объекта View прерывает выполнение запроса и освобождает ресурсы базы данных.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Метод View. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675642"
---
# <a name="viewclose-method"></a><span data-ttu-id="c21ad-103">Метод View. Close</span><span class="sxs-lookup"><span data-stu-id="c21ad-103">View.Close method</span></span>

<span data-ttu-id="c21ad-104">Метод **Close** объекта [**View**](view-object.md) прерывает выполнение запроса и освобождает ресурсы базы данных.</span><span class="sxs-lookup"><span data-stu-id="c21ad-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21ad-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c21ad-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="c21ad-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c21ad-106">Parameters</span></span>

<span data-ttu-id="c21ad-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c21ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c21ad-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c21ad-108">Return value</span></span>

<span data-ttu-id="c21ad-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c21ad-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c21ad-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c21ad-110">Remarks</span></span>

<span data-ttu-id="c21ad-111">Этот метод должен вызываться перед повторным вызовом метода [**EXECUTE**](view-execute.md) для объекта [**View**](view-object.md) , если только не были получены все строки результирующего набора с помощью метода [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="c21ad-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="c21ad-112">Он вызывается внутренним образом при уничтожении представления.</span><span class="sxs-lookup"><span data-stu-id="c21ad-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c21ad-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c21ad-113">Requirements</span></span>



| <span data-ttu-id="c21ad-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c21ad-114">Requirement</span></span> | <span data-ttu-id="c21ad-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c21ad-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21ad-116">Версия</span><span class="sxs-lookup"><span data-stu-id="c21ad-116">Version</span></span><br/> | <span data-ttu-id="c21ad-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c21ad-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c21ad-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c21ad-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c21ad-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="c21ad-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c21ad-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c21ad-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c21ad-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c21ad-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c21ad-122">IID</span><span class="sxs-lookup"><span data-stu-id="c21ad-122">IID</span></span><br/>     | <span data-ttu-id="c21ad-123">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c21ad-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




