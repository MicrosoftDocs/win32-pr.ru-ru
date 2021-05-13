---
description: Загружает список строк из реестра в список недавно использовавшихся (MRU).
title: 'Метод Иаклкустоммру:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841235"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="4eeb0-103">Метод Иаклкустоммру:: Initialize</span><span class="sxs-lookup"><span data-stu-id="4eeb0-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="4eeb0-104">Загружает список строк из реестра в список недавно использовавшихся (MRU).</span><span class="sxs-lookup"><span data-stu-id="4eeb0-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eeb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eeb0-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="4eeb0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eeb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eeb0-107">*пвсзмрурегкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eeb0-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eeb0-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="4eeb0-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="4eeb0-109">Указатель на буфер, содержащий раздел реестра со строками для списка MRU.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="4eeb0-110">*двмакс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4eeb0-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eeb0-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4eeb0-111">Type: **DWORD**</span></span>

<span data-ttu-id="4eeb0-112">Максимальное число записей, которые могут быть взяты из *пвсзмрурегкэй*.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eeb0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4eeb0-113">Return value</span></span>

<span data-ttu-id="4eeb0-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4eeb0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4eeb0-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4eeb0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4eeb0-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4eeb0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eeb0-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="4eeb0-117">Requirements</span></span>



| <span data-ttu-id="4eeb0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4eeb0-118">Requirement</span></span> | <span data-ttu-id="4eeb0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4eeb0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4eeb0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4eeb0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4eeb0-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4eeb0-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4eeb0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4eeb0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4eeb0-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4eeb0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




