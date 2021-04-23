---
description: Перевод гостевой службы в состояние запуска.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Метод Msvm_GuestService:: StartService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684685"
---
# <a name="msvm_guestservicestartservice-method"></a><span data-ttu-id="70283-103">Мсвм \_ гуестсервице:: StartService, метод</span><span class="sxs-lookup"><span data-stu-id="70283-103">Msvm\_GuestService::StartService method</span></span>

<span data-ttu-id="70283-104">Перевод гостевой службы в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="70283-104">Puts the guest service in a started state.</span></span>

## <a name="syntax"></a><span data-ttu-id="70283-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70283-105">Syntax</span></span>


```C++
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="70283-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70283-106">Parameters</span></span>

<span data-ttu-id="70283-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="70283-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70283-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70283-108">Return value</span></span>

<span data-ttu-id="70283-109">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="70283-109">This method returns one of the following values.</span></span>



| <span data-ttu-id="70283-110">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="70283-110">Return code/value</span></span>                                                                                                                                             | <span data-ttu-id="70283-111">Описание</span><span class="sxs-lookup"><span data-stu-id="70283-111">Description</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="70283-112"><dt>**Завершено без ошибки**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70283-112"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="70283-113">Успешно.</span><span class="sxs-lookup"><span data-stu-id="70283-113">Success.</span></span><br/> |
| <dl> <span data-ttu-id="70283-114"><dt>**Не поддерживается**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70283-114"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>           |                     |



 

## <a name="requirements"></a><span data-ttu-id="70283-115">Требования</span><span class="sxs-lookup"><span data-stu-id="70283-115">Requirements</span></span>



| <span data-ttu-id="70283-116">Требование</span><span class="sxs-lookup"><span data-stu-id="70283-116">Requirement</span></span> | <span data-ttu-id="70283-117">Значение</span><span class="sxs-lookup"><span data-stu-id="70283-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70283-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70283-118">Minimum supported client</span></span><br/> | <span data-ttu-id="70283-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="70283-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="70283-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70283-120">Minimum supported server</span></span><br/> | <span data-ttu-id="70283-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="70283-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70283-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70283-122">Namespace</span></span><br/>                | <span data-ttu-id="70283-123">\\\\Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="70283-123">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="70283-124">MOF</span><span class="sxs-lookup"><span data-stu-id="70283-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70283-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70283-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70283-126">DLL</span><span class="sxs-lookup"><span data-stu-id="70283-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70283-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70283-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70283-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70283-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70283-129">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="70283-129">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




