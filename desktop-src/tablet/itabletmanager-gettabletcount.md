---
description: Возвращает число планшетов, подключенных к системе.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'Метод Итаблетманажер:: Жеттаблеткаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272630"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="a6b88-103">Метод Итаблетманажер:: Жеттаблеткаунт</span><span class="sxs-lookup"><span data-stu-id="a6b88-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="a6b88-104">Возвращает число планшетов, подключенных к системе.</span><span class="sxs-lookup"><span data-stu-id="a6b88-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6b88-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="a6b88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6b88-107">*пктаблетс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a6b88-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b88-108">Число планшетов, подключенных к системе.</span><span class="sxs-lookup"><span data-stu-id="a6b88-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6b88-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6b88-109">Return value</span></span>

<span data-ttu-id="a6b88-110">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a6b88-110">This method can return one of these values.</span></span>



| <span data-ttu-id="a6b88-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a6b88-111">Return code</span></span>                                                                            | <span data-ttu-id="a6b88-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a6b88-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a6b88-113"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a6b88-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a6b88-114">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a6b88-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a6b88-115"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6b88-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a6b88-116">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a6b88-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6b88-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a6b88-117">Requirements</span></span>



| <span data-ttu-id="a6b88-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a6b88-118">Requirement</span></span> | <span data-ttu-id="a6b88-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a6b88-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b88-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6b88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b88-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6b88-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a6b88-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6b88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b88-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a6b88-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6b88-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6b88-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6b88-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6b88-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6b88-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6b88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b88-127">**Интерфейс Итаблетманажер**</span><span class="sxs-lookup"><span data-stu-id="a6b88-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 




