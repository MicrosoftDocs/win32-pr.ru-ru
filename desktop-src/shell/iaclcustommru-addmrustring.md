---
description: Добавляет запись в список недавно использовавшихся (MRU).
title: 'Метод Иаклкустоммру:: Аддмрустринг'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842005"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="19492-103">Метод Иаклкустоммру:: Аддмрустринг</span><span class="sxs-lookup"><span data-stu-id="19492-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="19492-104">Добавляет запись в список недавно использовавшихся (MRU).</span><span class="sxs-lookup"><span data-stu-id="19492-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="19492-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19492-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="19492-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19492-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19492-107">*пвсзентри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="19492-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19492-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="19492-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="19492-109">Указатель на буфер, содержащий новую запись.</span><span class="sxs-lookup"><span data-stu-id="19492-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19492-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19492-110">Return value</span></span>

<span data-ttu-id="19492-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="19492-111">Type: **HRESULT**</span></span>

<span data-ttu-id="19492-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="19492-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="19492-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19492-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="19492-114">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="19492-114">Requirements</span></span>



| <span data-ttu-id="19492-115">Требование</span><span class="sxs-lookup"><span data-stu-id="19492-115">Requirement</span></span> | <span data-ttu-id="19492-116">Значение</span><span class="sxs-lookup"><span data-stu-id="19492-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19492-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19492-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19492-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="19492-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="19492-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19492-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19492-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19492-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




