---
title: Метод Инапклиентманажемент Регистерсистемхеалсажент (Напманажемент. h)
description: Регистрирует SHA в системе защиты доступа к сети.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Метод Регистерсистемхеалсажент NAP
- Метод Регистерсистемхеалсажент NAP, интерфейс Инапклиентманажемент
- Инапклиентманажемент интерфейса NAP, метод Регистерсистемхеалсажент
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491709"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="bd09f-106">Метод Инапклиентманажемент:: Регистерсистемхеалсажент</span><span class="sxs-lookup"><span data-stu-id="bd09f-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="bd09f-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="bd09f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bd09f-108">Метод **регистерсистемхеалсажент** регистрирует SHA в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bd09f-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd09f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd09f-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="bd09f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd09f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd09f-111">*Агент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bd09f-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd09f-112">Указатель на структуру [**напкомпонентрегистратионинфо**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) , содержащую сведения о регистрации SHA.</span><span class="sxs-lookup"><span data-stu-id="bd09f-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd09f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd09f-113">Return value</span></span>

<span data-ttu-id="bd09f-114">Метод возвращает код состояния HRESULT, включая, помимо прочего, один из следующих.</span><span class="sxs-lookup"><span data-stu-id="bd09f-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="bd09f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bd09f-115">Return code</span></span>                                                                                            | <span data-ttu-id="bd09f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="bd09f-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd09f-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="bd09f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bd09f-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bd09f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="bd09f-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="bd09f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bd09f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="bd09f-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd09f-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bd09f-123"><dt>**\_ \_ конфликтующий идентификатор NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="bd09f-124">SHA, использующий этот идентификатор, уже зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="bd09f-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="bd09f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bd09f-125">Requirements</span></span>



| <span data-ttu-id="bd09f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bd09f-126">Requirement</span></span> | <span data-ttu-id="bd09f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bd09f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd09f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd09f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bd09f-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd09f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd09f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd09f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bd09f-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd09f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd09f-132">Header</span><span class="sxs-lookup"><span data-stu-id="bd09f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd09f-133"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd09f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="bd09f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd09f-135"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd09f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bd09f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd09f-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd09f-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="bd09f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd09f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd09f-139">**инапклиентманажемент**</span><span class="sxs-lookup"><span data-stu-id="bd09f-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





