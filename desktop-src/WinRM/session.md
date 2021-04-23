---
title: Объект Session (Всмандисп. h)
description: Определяет параметры операций и сеанса.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows объекта сеанса
- Служба удаленного управления Windows объекта сеанса, описание
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989407"
---
# <a name="session-object-wsmandisph"></a><span data-ttu-id="939eb-105">Объект Session (Всмандисп. h)</span><span class="sxs-lookup"><span data-stu-id="939eb-105">Session object (WSManDisp.h)</span></span>

<span data-ttu-id="939eb-106">Определяет параметры операций и сеанса.</span><span class="sxs-lookup"><span data-stu-id="939eb-106">Defines operations and session settings.</span></span> <span data-ttu-id="939eb-107">Любой служба удаленного управления Windows операции требует создания **сеанса** , который подключается к удаленному компьютеру, [*базовому контроллеру управления*](windows-remote-management-glossary.md) (BMC) или локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="939eb-107">Any Windows Remote Management operations require creation of a **Session** that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="939eb-108">Сетевые операции WinRM включают получение, запись или перечисление данных или вызов методов.</span><span class="sxs-lookup"><span data-stu-id="939eb-108">WinRM network operations include getting, writing, or enumerating data, or invoking methods.</span></span> <span data-ttu-id="939eb-109">Методы объекта **сеанса** зеркально отражают основные операции, определенные в протоколе WS-Management.</span><span class="sxs-lookup"><span data-stu-id="939eb-109">The methods of the **Session** object mirror the basic operations defined in the WS-Management protocol.</span></span>

## <a name="members"></a><span data-ttu-id="939eb-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="939eb-110">Members</span></span>

<span data-ttu-id="939eb-111">Объект **сеанса** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="939eb-111">The **Session** object has these types of members:</span></span>

-   [<span data-ttu-id="939eb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="939eb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="939eb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="939eb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="939eb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="939eb-114">Methods</span></span>

<span data-ttu-id="939eb-115">Объект **Session** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="939eb-115">The **Session** object has these methods.</span></span>



| <span data-ttu-id="939eb-116">Метод</span><span class="sxs-lookup"><span data-stu-id="939eb-116">Method</span></span>                                 | <span data-ttu-id="939eb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="939eb-117">Description</span></span>                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="939eb-118">**Создания**</span><span class="sxs-lookup"><span data-stu-id="939eb-118">**Create**</span></span>](session-create.md)       | <span data-ttu-id="939eb-119">Создает новый экземпляр ресурса и возвращает универсальный код ресурса (URI) нового объекта.</span><span class="sxs-lookup"><span data-stu-id="939eb-119">Creates a new instance of a resource and returns the URI of the new object.</span></span><br/>                                      |
| [<span data-ttu-id="939eb-120">**Удалить**</span><span class="sxs-lookup"><span data-stu-id="939eb-120">**Delete**</span></span>](session-delete.md)       | <span data-ttu-id="939eb-121">Удаляет ресурс, указанный в URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="939eb-121">Deletes the resource specified in the resource URI.</span></span><br/>                                                              |
| [<span data-ttu-id="939eb-122">**Перечислить**</span><span class="sxs-lookup"><span data-stu-id="939eb-122">**Enumerate**</span></span>](session-enumerate.md) | <span data-ttu-id="939eb-123">Перечисляет ресурсы журнала коллекции, таблицы или сообщения.</span><span class="sxs-lookup"><span data-stu-id="939eb-123">Enumerates a collection, table, or message log resource.</span></span><br/>                                                         |
| [<span data-ttu-id="939eb-124">**Получить**</span><span class="sxs-lookup"><span data-stu-id="939eb-124">**Get**</span></span>](session-get.md)             | <span data-ttu-id="939eb-125">Извлекает ресурс из службы и возвращает XML-представление текущего экземпляра ресурса.</span><span class="sxs-lookup"><span data-stu-id="939eb-125">Retrieves a resource from the service and returns an XML representation of the current instance of the resource.</span></span><br/> |
| [<span data-ttu-id="939eb-126">**Указывается**</span><span class="sxs-lookup"><span data-stu-id="939eb-126">**Identify**</span></span>](session-identify.md)   | <span data-ttu-id="939eb-127">Запрашивает удаленный компьютер, чтобы определить, поддерживает ли он протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="939eb-127">Queries a remote computer to determine if it supports the WS-Management protocol</span></span><br/>                                 |
| [<span data-ttu-id="939eb-128">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="939eb-128">**Invoke**</span></span>](session-invoke.md)       | <span data-ttu-id="939eb-129">Вызывает метод, возвращающий результаты вызова метода.</span><span class="sxs-lookup"><span data-stu-id="939eb-129">Invokes a method that returns the results of the method call.</span></span><br/>                                                    |
| [<span data-ttu-id="939eb-130">**PUT**</span><span class="sxs-lookup"><span data-stu-id="939eb-130">**Put**</span></span>](session-put.md)             | <span data-ttu-id="939eb-131">Обновление ресурса.</span><span class="sxs-lookup"><span data-stu-id="939eb-131">Updates a resource.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="939eb-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="939eb-132">Properties</span></span>

<span data-ttu-id="939eb-133">Объект **сеанса** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="939eb-133">The **Session** object has these properties.</span></span>



| <span data-ttu-id="939eb-134">Свойство</span><span class="sxs-lookup"><span data-stu-id="939eb-134">Property</span></span>                                            | <span data-ttu-id="939eb-135">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="939eb-135">Access type</span></span>           | <span data-ttu-id="939eb-136">Описание</span><span class="sxs-lookup"><span data-stu-id="939eb-136">Description</span></span>                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="939eb-137">**батчитемс**</span><span class="sxs-lookup"><span data-stu-id="939eb-137">**BatchItems**</span></span>](session-batchitems.md)<br/> | <span data-ttu-id="939eb-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="939eb-138">Read/write</span></span><br/> | <span data-ttu-id="939eb-139">Задает и возвращает количество элементов в каждом пакете перечисления.</span><span class="sxs-lookup"><span data-stu-id="939eb-139">Sets and gets the number of items in each enumeration batch.</span></span> <span data-ttu-id="939eb-140">Это значение нельзя изменить во время перечисления.</span><span class="sxs-lookup"><span data-stu-id="939eb-140">This value cannot be changed during an enumeration.</span></span> <span data-ttu-id="939eb-141">По умолчанию значение по умолчанию равно неограниченному количеству элементов.</span><span class="sxs-lookup"><span data-stu-id="939eb-141">By default, the default is an unlimited number of items.</span></span> <span data-ttu-id="939eb-142">Поставщик ресурсов может установить ограничение.</span><span class="sxs-lookup"><span data-stu-id="939eb-142">The resource provider may set a limit.</span></span><br/> |
| [<span data-ttu-id="939eb-143">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="939eb-143">**Error**</span></span>](session-error.md)<br/>           | <span data-ttu-id="939eb-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="939eb-144">Read-only</span></span><br/>  | <span data-ttu-id="939eb-145">Возвращает дополнительные сведения об ошибке в потоке XML.</span><span class="sxs-lookup"><span data-stu-id="939eb-145">Gets additional error information in an XML stream.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="939eb-146">**Счетчик**</span><span class="sxs-lookup"><span data-stu-id="939eb-146">**Timeout**</span></span>](session-timeout.md)<br/>       | <span data-ttu-id="939eb-147">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="939eb-147">Read/write</span></span><br/> | <span data-ttu-id="939eb-148">Задает и возвращает максимальное время ожидания (в миллисекундах) для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="939eb-148">Sets and gets the maximum amount of time (in milliseconds) for the client application to wait.</span></span><br/>                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="939eb-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="939eb-149">Remarks</span></span>

<span data-ttu-id="939eb-150">Объект **Session** соответствует интерфейсу [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .</span><span class="sxs-lookup"><span data-stu-id="939eb-150">The **Session** object corresponds to the [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="939eb-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="939eb-151">Examples</span></span>

<span data-ttu-id="939eb-152">В следующем примере кода VBScript показано, как создать объект **сеанса** .</span><span class="sxs-lookup"><span data-stu-id="939eb-152">The following VBScript code example shows how to create a **Session** object.</span></span>


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a><span data-ttu-id="939eb-153">Требования</span><span class="sxs-lookup"><span data-stu-id="939eb-153">Requirements</span></span>



| <span data-ttu-id="939eb-154">Требование</span><span class="sxs-lookup"><span data-stu-id="939eb-154">Requirement</span></span> | <span data-ttu-id="939eb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="939eb-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="939eb-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="939eb-156">Minimum supported client</span></span><br/> | <span data-ttu-id="939eb-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="939eb-157">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="939eb-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="939eb-158">Minimum supported server</span></span><br/> | <span data-ttu-id="939eb-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="939eb-159">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="939eb-160">Header</span><span class="sxs-lookup"><span data-stu-id="939eb-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="939eb-161"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="939eb-161"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="939eb-162">IDL</span><span class="sxs-lookup"><span data-stu-id="939eb-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="939eb-163"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="939eb-163"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="939eb-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="939eb-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="939eb-165"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="939eb-165"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="939eb-166">DLL</span><span class="sxs-lookup"><span data-stu-id="939eb-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="939eb-167"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="939eb-167"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="939eb-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="939eb-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939eb-169">API сценариев WinRM</span><span class="sxs-lookup"><span data-stu-id="939eb-169">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="939eb-170">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="939eb-170">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="939eb-171">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="939eb-171">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="939eb-172">Создание сценариев в служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="939eb-172">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="939eb-173">Получение данных с локального компьютера</span><span class="sxs-lookup"><span data-stu-id="939eb-173">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="939eb-174">Получение данных с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="939eb-174">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





