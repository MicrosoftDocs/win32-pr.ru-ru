---
title: Метод Инапсистемхеалсаженткаллбакк Жетфиксупинфо (Напсистемхеалсажент. h)
description: Вызывается Напажент для определения состояния агента работоспособности системы во время обработки Сохреспонсе.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Метод Жетфиксупинфо NAP
- Метод Жетфиксупинфо NAP, интерфейс Инапсистемхеалсаженткаллбакк
- Инапсистемхеалсаженткаллбакк интерфейса NAP, метод Жетфиксупинфо
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136206"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="0412b-106">Метод Инапсистемхеалсаженткаллбакк:: Жетфиксупинфо</span><span class="sxs-lookup"><span data-stu-id="0412b-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="0412b-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0412b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0412b-108">Метод **инапсистемхеалсаженткаллбакк:: жетфиксупинфо** вызывается напажент для определения состояния агента работоспособности системы во время обработки [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="0412b-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="0412b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0412b-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="0412b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0412b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0412b-111">*сведения о* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0412b-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0412b-112">Указатель на указатель на структуру [**фиксупинфо**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) , которая содержит состояние исправления агента.</span><span class="sxs-lookup"><span data-stu-id="0412b-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0412b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0412b-113">Return value</span></span>

<span data-ttu-id="0412b-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0412b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0412b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0412b-115">Return code</span></span>                                                                          | <span data-ttu-id="0412b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0412b-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="0412b-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0412b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0412b-118">Указывает на успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="0412b-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0412b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0412b-119">Remarks</span></span>

<span data-ttu-id="0412b-120">Этот метод обратного вызова объявляется системой защиты доступа к сети и реализуется модулем записи SHA.</span><span class="sxs-lookup"><span data-stu-id="0412b-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="0412b-121">Агент работоспособности системы должен вернуть значение **S \_ ОК** немедленно без блокировки.</span><span class="sxs-lookup"><span data-stu-id="0412b-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="0412b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0412b-122">Requirements</span></span>



| <span data-ttu-id="0412b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0412b-123">Requirement</span></span> | <span data-ttu-id="0412b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0412b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0412b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0412b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0412b-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0412b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0412b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0412b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0412b-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0412b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0412b-129">Header</span><span class="sxs-lookup"><span data-stu-id="0412b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0412b-130"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="0412b-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0412b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="0412b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0412b-132"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0412b-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0412b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0412b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0412b-134">**инапсистемхеалсаженткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="0412b-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





