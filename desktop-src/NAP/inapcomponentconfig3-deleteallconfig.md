---
title: Метод INapComponentConfig3 Делетеаллконфиг (Напкоммон. h)
description: Реализуется средствами проверки работоспособности системы (SHV) для предоставления способа сброса хранилища SHV в исходное состояние после установки.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Метод Делетеаллконфиг NAP
- Метод Делетеаллконфиг NAP, интерфейс INapComponentConfig3
- INapComponentConfig3 интерфейса NAP, метод Делетеаллконфиг
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891689"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="7ccfe-106">INapComponentConfig3: метод:D Елетеаллконфиг</span><span class="sxs-lookup"><span data-stu-id="7ccfe-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="7ccfe-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7ccfe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7ccfe-108">Метод **делетеаллконфиг** реализуется средствами проверки работоспособности системы (SHV) для предоставления способа сброса хранилища SHV в исходное состояние после установки.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="7ccfe-109">Все данные конфигурации, кроме конфигурации по умолчанию, должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ccfe-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ccfe-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="7ccfe-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ccfe-111">Parameters</span></span>

<span data-ttu-id="7ccfe-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ccfe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ccfe-113">Return value</span></span>

<span data-ttu-id="7ccfe-114">Возвращает один из следующих кодов ошибок в зависимости от результата этой операции.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="7ccfe-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7ccfe-115">Return code</span></span>                                                                           | <span data-ttu-id="7ccfe-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7ccfe-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7ccfe-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7ccfe-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="7ccfe-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="7ccfe-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ccfe-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7ccfe-119">Requirements</span></span>



| <span data-ttu-id="7ccfe-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7ccfe-120">Requirement</span></span> | <span data-ttu-id="7ccfe-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccfe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccfe-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ccfe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccfe-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ccfe-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7ccfe-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ccfe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccfe-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ccfe-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7ccfe-126">Header</span><span class="sxs-lookup"><span data-stu-id="7ccfe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ccfe-127"><dt>Напкоммон. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ccfe-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ccfe-128">IDL</span><span class="sxs-lookup"><span data-stu-id="7ccfe-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ccfe-129"><dt>Напкоммон. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ccfe-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ccfe-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ccfe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccfe-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="7ccfe-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





