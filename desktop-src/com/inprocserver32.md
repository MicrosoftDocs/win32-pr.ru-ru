---
title: InprocServer32
description: Регистрирует 32-разрядный внутрипроцессный сервер и задает потоковую модель апартамента, в которой может работать сервер.
ms.assetid: 4edbbd9d-7ea1-4476-aee7-eaf30e54db8d
keywords:
- COM раздела реестра InprocServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daae9d495ad588e0dc710b63fe7d7ae9f48c11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532345"
---
# <a name="inprocserver32"></a><span data-ttu-id="8e4f7-104">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="8e4f7-104">InprocServer32</span></span>

<span data-ttu-id="8e4f7-105">Регистрирует 32-разрядный внутрипроцессный сервер и задает потоковую модель апартамента, в которой может работать сервер.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-105">Registers a 32-bit in-process server and specifies the threading model of the apartment the server can run in.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8e4f7-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="8e4f7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer32
         (Default) = path
         ThreadingModel = value
```

## <a name="remarks"></a><span data-ttu-id="8e4f7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e4f7-107">Remarks</span></span>

<span data-ttu-id="8e4f7-108">**ThreadingModel** — это значение **reg \_ SZ** , указывающее потоковую модель.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-108">**ThreadingModel** is a **REG\_SZ** value the specifies the threading model.</span></span> <span data-ttu-id="8e4f7-109">Возможные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-109">The possible values are shown in the following table.</span></span>



| <span data-ttu-id="8e4f7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-110">Value</span></span>     | <span data-ttu-id="8e4f7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8e4f7-111">Description</span></span>                                |
|-----------|--------------------------------------------|
| <span data-ttu-id="8e4f7-112">Разделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-112">Apartment</span></span> | <span data-ttu-id="8e4f7-113">Однопотоковое подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-113">Single-threaded apartment</span></span>                  |
| <span data-ttu-id="8e4f7-114">Оба</span><span class="sxs-lookup"><span data-stu-id="8e4f7-114">Both</span></span>      | <span data-ttu-id="8e4f7-115">Однопотоковое или многопоточное подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-115">Single-threaded or multithreaded apartment</span></span> |
| <span data-ttu-id="8e4f7-116">Бесплатный</span><span class="sxs-lookup"><span data-stu-id="8e4f7-116">Free</span></span>      | <span data-ttu-id="8e4f7-117">Многопоточное подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-117">Multithreaded apartment</span></span>                    |
| <span data-ttu-id="8e4f7-118">нейтральное выражение.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-118">Neutral</span></span>   | <span data-ttu-id="8e4f7-119">Нейтральное подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-119">Neutral apartment</span></span>                          |



 

<span data-ttu-id="8e4f7-120">Для каждого объекта, предоставленного внутрипроцессного сервером, необходимо использовать одно и то же значение.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-120">You must use the same value for every object provided by the in-process server.</span></span>

<span data-ttu-id="8e4f7-121">Если **ThreadingModel** отсутствует или не задано значение, сервер загружается в первый апартамент, инициализированный в процессе.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-121">If **ThreadingModel** is not present or is not set to a value, the server is loaded into the first apartment that was initialized in the process.</span></span> <span data-ttu-id="8e4f7-122">Этот апартамент иногда называют основным однопотоковым апартаментом (STA).</span><span class="sxs-lookup"><span data-stu-id="8e4f7-122">This apartment is sometimes referred to as the main single-threaded apartment (STA).</span></span> <span data-ttu-id="8e4f7-123">Если первый поток STA в процессе инициализируется моделью COM, а не явным вызовом [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), он называется главным STA.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-123">If the first STA in a process is initialized by COM, rather than by an explicit call to [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), it is called the host STA.</span></span> <span data-ttu-id="8e4f7-124">Например, COM создает главный STA, если внутрипроцессный сервер, который требуется загрузить, требует STA, но в данный момент в процессе нет STA.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-124">For example, COM creates a host STA if an in-process server to be loaded requires an STA but there is currently no STA in the process.</span></span>

<span data-ttu-id="8e4f7-125">Когда это возможно, внутрипроцессный сервер загружается в тот же апартамент, что и клиент, который его загружает.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-125">Whenever possible, the in-process server is loaded in the same apartment as the client that loads it.</span></span> <span data-ttu-id="8e4f7-126">Если потоковая модель подразделения клиента несовместима с указанной моделью, сервер загружается, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-126">If the threading model of the client apartment is not compatible with the model specified, the server is loaded as indicated in the following table.</span></span>



| <span data-ttu-id="8e4f7-127">Потоковая модель сервера</span><span class="sxs-lookup"><span data-stu-id="8e4f7-127">Threading model of server</span></span> | <span data-ttu-id="8e4f7-128">Сервер подразделения запущен в</span><span class="sxs-lookup"><span data-stu-id="8e4f7-128">Apartment server is run in</span></span> |
|---------------------------|----------------------------|
| <not specified>     | <span data-ttu-id="8e4f7-129">Главный STA</span><span class="sxs-lookup"><span data-stu-id="8e4f7-129">Main STA</span></span>                   |
| <span data-ttu-id="8e4f7-130">Оба</span><span class="sxs-lookup"><span data-stu-id="8e4f7-130">Both</span></span>                      | <span data-ttu-id="8e4f7-131">Тот же апартамент, что и клиент</span><span class="sxs-lookup"><span data-stu-id="8e4f7-131">Same apartment as client</span></span>   |
| <span data-ttu-id="8e4f7-132">Бесплатный</span><span class="sxs-lookup"><span data-stu-id="8e4f7-132">Free</span></span>                      | <span data-ttu-id="8e4f7-133">Многопоточное подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-133">Multithreaded apartment</span></span>    |
| <span data-ttu-id="8e4f7-134">нейтральное выражение.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-134">Neutral</span></span>                   | <span data-ttu-id="8e4f7-135">Нейтральное подразделение</span><span class="sxs-lookup"><span data-stu-id="8e4f7-135">Neutral apartment</span></span>          |



 

<span data-ttu-id="8e4f7-136">Если потоковая модель сервера является Апартаментной, то подразделение, в котором загружен сервер, зависит от апартамента, в котором выполняется клиент, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-136">If the threading model of the server is Apartment, the apartment the server is loaded in depends on the apartment the client is running in, as indicated in the following table.</span></span>



| <span data-ttu-id="8e4f7-137">Клиент подразделения запущен в</span><span class="sxs-lookup"><span data-stu-id="8e4f7-137">Apartment client is run in</span></span> | <span data-ttu-id="8e4f7-138">Сервер подразделения запущен в</span><span class="sxs-lookup"><span data-stu-id="8e4f7-138">Apartment server is run in</span></span> |
|----------------------------|----------------------------|
| <span data-ttu-id="8e4f7-139">Многопоточных</span><span class="sxs-lookup"><span data-stu-id="8e4f7-139">Multithreaded</span></span>              | <span data-ttu-id="8e4f7-140">Главный STA</span><span class="sxs-lookup"><span data-stu-id="8e4f7-140">Host STA</span></span>                   |
| <span data-ttu-id="8e4f7-141">Нейтральный (в потоке STA)</span><span class="sxs-lookup"><span data-stu-id="8e4f7-141">Neutral (on STA thread)</span></span>    | <span data-ttu-id="8e4f7-142">Тот же апартамент, что и клиент</span><span class="sxs-lookup"><span data-stu-id="8e4f7-142">Same apartment as client</span></span>   |
| <span data-ttu-id="8e4f7-143">Нейтральный (в потоке MTA)</span><span class="sxs-lookup"><span data-stu-id="8e4f7-143">Neutral (on MTA thread)</span></span>    | <span data-ttu-id="8e4f7-144">Главный STA</span><span class="sxs-lookup"><span data-stu-id="8e4f7-144">Host STA</span></span>                   |



 

<span data-ttu-id="8e4f7-145">COM также может создать многопотоковый апартамент узла (MTA).</span><span class="sxs-lookup"><span data-stu-id="8e4f7-145">COM can also create a host multithreaded apartment (MTA).</span></span> <span data-ttu-id="8e4f7-146">Если клиент в однопотоковом апартаменте запрашивает внутрипроцессный сервер, модель потоков которого свободна, если в процессе нет агента передачи сообщений, COM создает агент передачи узла и загружает в него сервер.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-146">If a client in a single-threaded apartment requests an in-process server whose threading model is Free when there is no MTA in the process, COM creates a host MTA and loads the server into it.</span></span>

<span data-ttu-id="8e4f7-147">Для 32-разрядного внутрипроцессного сервера необходимо зарегистрировать [**InprocHandler32**](inprochandler32.md), [**инпроксервер**](inprocserver.md), **InprocServer32** и [**вставляемые**](insertable.md) ключи.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-147">For a 32-bit in-process server, the [**InprocHandler32**](inprochandler32.md), [**InprocServer**](inprocserver.md), **InprocServer32**, and [**Insertable**](insertable.md) keys must be registered.</span></span> <span data-ttu-id="8e4f7-148">Запись **инпроксервер** необходима только для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-148">The **InprocServer** entry is needed only for backward compatibility.</span></span> <span data-ttu-id="8e4f7-149">Если он отсутствует, класс по-прежнему работает, но не может быть загружен в 16-разрядные приложения.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-149">If it is missing, the class still works but it cannot be loaded in 16-bit applications.</span></span>

<span data-ttu-id="8e4f7-150">Если контейнер выполняет поиск в реестре внутрипроцессного сервера, 16-разрядная версия имеет приоритет с 16-разрядным контейнером, а 32-разрядная версия имеет приоритет с 32-битным контейнером.</span><span class="sxs-lookup"><span data-stu-id="8e4f7-150">If a container is searching the registry for an in-process server, the 16-bit version has priority with a 16-bit container and the 32-bit version has priority with a 32-bit container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e4f7-151">См. также</span><span class="sxs-lookup"><span data-stu-id="8e4f7-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e4f7-152">**инпроксервер**</span><span class="sxs-lookup"><span data-stu-id="8e4f7-152">**InprocServer**</span></span>](inprocserver.md)
</dt> </dl>

 

 




