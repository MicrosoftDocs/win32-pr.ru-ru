---
description: Метод GetObject объекта View возвращает ошибку проверки и имя столбца, для которого произошла ошибка.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Метод View. с ошибками
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651753"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="65c2a-103">Метод View. с ошибками</span><span class="sxs-lookup"><span data-stu-id="65c2a-103">View.GetError method</span></span>

<span data-ttu-id="65c2a-104">Метод GetObject объекта [**View**](view-object.md) **возвращает ошибку проверки** и имя столбца, для которого произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="65c2a-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="65c2a-105">В службе автоматизации возвращаемое значение является строкой вида \# \# ColumnName, где — \# \# 2-значный код ошибки.</span><span class="sxs-lookup"><span data-stu-id="65c2a-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="65c2a-106">Он возвращает первую ошибку в массиве ошибок представления. последующие вызовы возвращают следующее значение в массиве ошибок.</span><span class="sxs-lookup"><span data-stu-id="65c2a-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="65c2a-107">После возвращения значения "00" больше ошибок не существует, и последующие вызовы просто проводят через массив снова.</span><span class="sxs-lookup"><span data-stu-id="65c2a-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65c2a-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="65c2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="65c2a-109">Parameters</span></span>

<span data-ttu-id="65c2a-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="65c2a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65c2a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65c2a-111">Return value</span></span>

<span data-ttu-id="65c2a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="65c2a-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c2a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="65c2a-113">Requirements</span></span>



| <span data-ttu-id="65c2a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="65c2a-114">Requirement</span></span> | <span data-ttu-id="65c2a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="65c2a-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c2a-116">Версия</span><span class="sxs-lookup"><span data-stu-id="65c2a-116">Version</span></span><br/> | <span data-ttu-id="65c2a-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65c2a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="65c2a-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="65c2a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="65c2a-119">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="65c2a-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="65c2a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="65c2a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="65c2a-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65c2a-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="65c2a-122">IID</span><span class="sxs-lookup"><span data-stu-id="65c2a-122">IID</span></span><br/>     | <span data-ttu-id="65c2a-123">IID \_ IView определен как 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="65c2a-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




