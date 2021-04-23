---
title: Метод Инапклиентманажемент Регистеренфорцементклиент (Напманажемент. h)
description: Регистрирует клиент принудительного применения в системе защиты доступа к сети.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Метод Регистеренфорцементклиент NAP
- Метод Регистеренфорцементклиент NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Регистеренфорцементклиент
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136575"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="6e6fe-106">Метод Инапклиентманажемент:: Регистеренфорцементклиент</span><span class="sxs-lookup"><span data-stu-id="6e6fe-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="6e6fe-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e6fe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6e6fe-108">Метод **регистеренфорцементклиент** регистрирует клиент принудительного применения в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6fe-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e6fe-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="6e6fe-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e6fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e6fe-111">*принудительное применение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e6fe-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e6fe-112">Указатель на структуру данных [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации, связанные с клиентом принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e6fe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e6fe-113">Return value</span></span>

<span data-ttu-id="6e6fe-114">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="6e6fe-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6e6fe-115">Return code</span></span>                                                                                            | <span data-ttu-id="6e6fe-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6e6fe-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e6fe-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6e6fe-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="6e6fe-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="6e6fe-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6e6fe-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="6e6fe-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="6e6fe-123"><dt>**\_ \_ конфликтующий идентификатор NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="6e6fe-124">Агент принудительного применения, использующий данный идентификатор, уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="6e6fe-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e6fe-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6e6fe-125">Requirements</span></span>



| <span data-ttu-id="6e6fe-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6e6fe-126">Requirement</span></span> | <span data-ttu-id="6e6fe-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6e6fe-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6fe-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e6fe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e6fe-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e6fe-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e6fe-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e6fe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e6fe-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e6fe-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6e6fe-132">Header</span><span class="sxs-lookup"><span data-stu-id="6e6fe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e6fe-133"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e6fe-134">IDL</span><span class="sxs-lookup"><span data-stu-id="6e6fe-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e6fe-135"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e6fe-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6e6fe-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e6fe-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e6fe-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="6e6fe-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e6fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6fe-139">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="6e6fe-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





