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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997686"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="32d65-103">Метод Иаклкустоммру:: Аддмрустринг</span><span class="sxs-lookup"><span data-stu-id="32d65-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="32d65-104">Добавляет запись в список недавно использовавшихся (MRU).</span><span class="sxs-lookup"><span data-stu-id="32d65-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32d65-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="32d65-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32d65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d65-107">*пвсзентри* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="32d65-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32d65-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="32d65-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="32d65-109">Указатель на буфер, содержащий новую запись.</span><span class="sxs-lookup"><span data-stu-id="32d65-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d65-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32d65-110">Return value</span></span>

<span data-ttu-id="32d65-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="32d65-111">Type: **HRESULT**</span></span>

<span data-ttu-id="32d65-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="32d65-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="32d65-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="32d65-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="32d65-114">Требования</span><span class="sxs-lookup"><span data-stu-id="32d65-114">Requirements</span></span>



| <span data-ttu-id="32d65-115">Требование</span><span class="sxs-lookup"><span data-stu-id="32d65-115">Requirement</span></span> | <span data-ttu-id="32d65-116">Значение</span><span class="sxs-lookup"><span data-stu-id="32d65-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32d65-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32d65-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32d65-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="32d65-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="32d65-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32d65-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32d65-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32d65-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




