---
description: Позволяет открывать и управлять подключением к смарт-карте.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Интерфейс кредитной карты (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544226"
---
# <a name="iscard-interface"></a><span data-ttu-id="d7a1e-103">Интерфейс кредитной карты</span><span class="sxs-lookup"><span data-stu-id="d7a1e-103">ISCard interface</span></span>

<span data-ttu-id="d7a1e-104">\[Интерфейс **кредитной карты** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7a1e-105">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="d7a1e-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d7a1e-106">Интерфейс **кредитной карты** позволяет открывать [*смарт-карту*](../secgloss/s-gly.md)и управлять ей.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d7a1e-107">Для каждого соединения с картой требуется один соответствующий экземпляр интерфейса- **карты** .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="d7a1e-108">[*Диспетчер ресурсов*](../secgloss/r-gly.md) смарт-карт должен быть доступен всякий раз, когда создается экземпляр класса « **открытка** ».</span><span class="sxs-lookup"><span data-stu-id="d7a1e-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="d7a1e-109">Если эта служба недоступна, создание интерфейса завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="d7a1e-110">В следующем примере показано типичное использование интерфейса- **карты** .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="d7a1e-111">Интерфейс **кредитной** карты используется для подключения к смарт-карте, отправки [*транзакции*](../secgloss/t-gly.md)и освобождения смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="d7a1e-112">**Отправка транзакции на определенную карточку**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="d7a1e-113">Создайте интерфейс **кредитной карты** .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="d7a1e-114">Подключитесь к смарт-карте, указав [*устройство чтения*](../secgloss/r-gly.md) смарт-карт или используя ранее установленный, допустимый маркер.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="d7a1e-115">Создание команд транзакций с помощью [**искардкмд**](iscardcmd.md)и [**ISCardISO7816**](iscardiso7816.md) интерфейсов смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="d7a1e-116">Используйте команду "Submit **", чтобы** отправить команды транзакции для обработки со смарт-картой.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="d7a1e-117">Используйте для освобождения смарт **-карты.**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="d7a1e-118">Освободите интерфейс **кредитной карты** .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="d7a1e-119">Элементы</span><span class="sxs-lookup"><span data-stu-id="d7a1e-119">Members</span></span>

<span data-ttu-id="d7a1e-120">Интерфейс **кредитной карты** наследует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d7a1e-121">У **карточки** также есть члены следующих типов:</span><span class="sxs-lookup"><span data-stu-id="d7a1e-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="d7a1e-122">Методы</span><span class="sxs-lookup"><span data-stu-id="d7a1e-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7a1e-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="d7a1e-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7a1e-124">Методы</span><span class="sxs-lookup"><span data-stu-id="d7a1e-124">Methods</span></span>

<span data-ttu-id="d7a1e-125">Интерфейс **кредитной карты** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="d7a1e-126">Метод</span><span class="sxs-lookup"><span data-stu-id="d7a1e-126">Method</span></span>                                          | <span data-ttu-id="d7a1e-127">Описание</span><span class="sxs-lookup"><span data-stu-id="d7a1e-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7a1e-128">**аттачбихандле**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="d7a1e-129">Присоединяет объект к открытому и настроенному обработчику смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="d7a1e-130">**аттачбиреадер**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="d7a1e-131">Открывает смарт-карту в именованном модуле чтения.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="d7a1e-132">**Соединил**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="d7a1e-133">Закрывает открытое подключение к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="d7a1e-134">**локкскард**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="d7a1e-135">Потребует монопольного доступа к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="d7a1e-136">**Повторно подключиться**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="d7a1e-137">Сбрасывает и повторно инициализирует смарт-карту.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="d7a1e-138">**Транзакция**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="d7a1e-139">Выполняет операцию записи и чтения для объекта команды смарт-карты ([*блок данных протокола приложения*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="d7a1e-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="d7a1e-140">**унлоккскард**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="d7a1e-141">Освобождает эксклюзивный доступ к смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="d7a1e-142">Свойства</span><span class="sxs-lookup"><span data-stu-id="d7a1e-142">Properties</span></span>

<span data-ttu-id="d7a1e-143">Интерфейс **кредитной карты** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="d7a1e-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="d7a1e-144">Property</span></span>                                               | <span data-ttu-id="d7a1e-145">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d7a1e-145">Access type</span></span>          | <span data-ttu-id="d7a1e-146">Описание</span><span class="sxs-lookup"><span data-stu-id="d7a1e-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7a1e-147">**Допустимо**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="d7a1e-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7a1e-148">Read-only</span></span><br/> | <span data-ttu-id="d7a1e-149">Извлекает [*строку ATR*](../secgloss/a-gly.md) смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="d7a1e-150">**кардхандле**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="d7a1e-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7a1e-151">Read-only</span></span><br/> | <span data-ttu-id="d7a1e-152">Извлекает маркер подключенной смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d7a1e-153">**Локального**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="d7a1e-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7a1e-154">Read-only</span></span><br/> | <span data-ttu-id="d7a1e-155">Извлекает текущий маркер [*контекста диспетчера ресурсов*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="d7a1e-156">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="d7a1e-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7a1e-157">Read-only</span></span><br/> | <span data-ttu-id="d7a1e-158">Возвращает идентификатор протокола, используемого в данный момент на смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="d7a1e-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d7a1e-159">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d7a1e-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="d7a1e-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d7a1e-160">Read-only</span></span><br/> | <span data-ttu-id="d7a1e-161">Извлекает текущее [*состояние*](../secgloss/s-gly.md) , в котором находится [*смарт-карта*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a1e-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d7a1e-162">Требования</span><span class="sxs-lookup"><span data-stu-id="d7a1e-162">Requirements</span></span>



| <span data-ttu-id="d7a1e-163">Требование</span><span class="sxs-lookup"><span data-stu-id="d7a1e-163">Requirement</span></span> | <span data-ttu-id="d7a1e-164">Значение</span><span class="sxs-lookup"><span data-stu-id="d7a1e-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a1e-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7a1e-165">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a1e-166">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7a1e-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7a1e-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7a1e-167">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a1e-168">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7a1e-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7a1e-169">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d7a1e-169">End of client support</span></span><br/>    | <span data-ttu-id="d7a1e-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7a1e-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d7a1e-171">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d7a1e-171">End of server support</span></span><br/>    | <span data-ttu-id="d7a1e-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7a1e-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d7a1e-173">Header</span><span class="sxs-lookup"><span data-stu-id="d7a1e-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a1e-174"><dt>Скардмгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a1e-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7a1e-175">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d7a1e-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7a1e-176"><dt>Скардмгр. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7a1e-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7a1e-177">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a1e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a1e-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a1e-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7a1e-179">IID</span><span class="sxs-lookup"><span data-stu-id="d7a1e-179">IID</span></span><br/>                      | <span data-ttu-id="d7a1e-180">Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d7a1e-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
