---
description: Моникер очереди используется для активации компонента очереди программным способом.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Использование моникера очереди
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701222"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="eafab-103">Использование моникера очереди</span><span class="sxs-lookup"><span data-stu-id="eafab-103">Using the Queue Moniker</span></span>

<span data-ttu-id="eafab-104">Моникер очереди используется для активации компонента очереди программным способом.</span><span class="sxs-lookup"><span data-stu-id="eafab-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="eafab-105">Моникер очереди требует, чтобы он получал идентификатор класса (CLSID) объекта для вызова из нового моникера непосредственно справа от него.</span><span class="sxs-lookup"><span data-stu-id="eafab-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="eafab-106">При использовании префикса слева новый моникер передает CLSID в моникер слева от него.</span><span class="sxs-lookup"><span data-stu-id="eafab-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="eafab-107">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="eafab-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="eafab-108">Не применяется.</span><span class="sxs-lookup"><span data-stu-id="eafab-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="eafab-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="eafab-109">Visual Basic</span></span>

<span data-ttu-id="eafab-110">Параметр отображаемого имени GetObject имеет значение "Queue:/New:", за которым следует идентификатор программы или идентификатор GUID строкового типа (или без фигурных скобок) объекта сервера, для которого создается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="eafab-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="eafab-111">В следующих примерах показаны три допустимые активации компонента с моникером очереди:</span><span class="sxs-lookup"><span data-stu-id="eafab-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="eafab-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="eafab-112">C/C++</span></span>

<span data-ttu-id="eafab-113">Параметр отображаемого имени [**кожетобжект**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) имеет значение "Queue:/New:", за которым следует идентификатор программы или идентификатор GUID строкового типа (или без фигурных скобок) объекта сервера, для которого создается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="eafab-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="eafab-114">В следующих примерах показаны три допустимые активации компонента с моникером очереди:</span><span class="sxs-lookup"><span data-stu-id="eafab-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="eafab-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eafab-115">Remarks</span></span>

<span data-ttu-id="eafab-116">Моникер очереди принимает необязательные параметры, которые изменяют свойства сообщения, отправляемого в очередь сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="eafab-117">Например, чтобы сообщение очереди сообщений было отправлено с приоритетом 6, компонент очереди будет активирован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eafab-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="eafab-118">В следующей таблице перечислены параметры моникера очереди, влияющие на очередь назначения.</span><span class="sxs-lookup"><span data-stu-id="eafab-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eafab-119">Параметр</span><span class="sxs-lookup"><span data-stu-id="eafab-119">Parameter</span></span></th>
<th><span data-ttu-id="eafab-120">Описание</span><span class="sxs-lookup"><span data-stu-id="eafab-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eafab-121"><em>ИмяКомпьютера</em></span><span class="sxs-lookup"><span data-stu-id="eafab-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="eafab-122">Указывает часть имени компьютера в пути очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="eafab-123">Путь очереди очереди сообщений имеет формат <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="eafab-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="eafab-124">Если не указано, используется имя компьютера, связанное с настроенным приложением.</span><span class="sxs-lookup"><span data-stu-id="eafab-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="eafab-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="eafab-126">Указывает имя очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="eafab-127">Путь очереди очереди сообщений имеет формат <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="eafab-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="eafab-128">Если не указано, используется имя очереди, связанное с настроенным приложением.</span><span class="sxs-lookup"><span data-stu-id="eafab-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="eafab-129">Чтобы получить нетранзакционную очередь, сначала можно указать имя очереди, а затем создать приложение COM+ с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="eafab-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="eafab-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="eafab-131">Указывает полное имя пути очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="eafab-132">Если этот параметр не указан, используется имя пути очереди сообщений, связанное с настроенным приложением.</span><span class="sxs-lookup"><span data-stu-id="eafab-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="eafab-133">Чтобы переопределить имя назначения, путь можно указать в следующей форме для установки рабочей группы очереди сообщений:</span><span class="sxs-lookup"><span data-stu-id="eafab-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="eafab-134">Queue:<em>PathName</em> = <em>имя_компьютера</em>\привате $ \ AppName/New: MyProject. кмикласс</span><span class="sxs-lookup"><span data-stu-id="eafab-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="eafab-135">Для языков программирования C и Microsoft Visual C++ требуется две обратные косые черты, представляющие одну обратную косую кавычки в строковых литералах, например, в Чикаго \\ .</span><span class="sxs-lookup"><span data-stu-id="eafab-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-136"><em>FormatName</em></span><span class="sxs-lookup"><span data-stu-id="eafab-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="eafab-137">Если приложение COM+ помечается как поставленное в очередь, COM+ создает очередь сообщений, имя которой совпадает с именем приложения.</span><span class="sxs-lookup"><span data-stu-id="eafab-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="eafab-138">Имя формата очереди сообщений в этой очереди находится в каталоге COM+, связанном с приложением COM+.</span><span class="sxs-lookup"><span data-stu-id="eafab-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="eafab-139">Чтобы переопределить имя назначения, можно указать имя формата в следующей форме для установки рабочей группы очереди сообщений:</span><span class="sxs-lookup"><span data-stu-id="eafab-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="eafab-140">Очередь:<em>FormatName</em>= Direct = OS:<em>имя_компьютера</em>\привате $ \ AppName/New: ProgID</span><span class="sxs-lookup"><span data-stu-id="eafab-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="eafab-141">В конфигурации Active Directory &quot; частный $ &quot; не указывается как часть имени очереди.</span><span class="sxs-lookup"><span data-stu-id="eafab-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="eafab-142">Необязательные параметры моникера очереди обрабатываются слева направо.</span><span class="sxs-lookup"><span data-stu-id="eafab-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="eafab-143">Указывайте каждое ключевое слово только один раз.</span><span class="sxs-lookup"><span data-stu-id="eafab-143">Specify each keyword only one time.</span></span> <span data-ttu-id="eafab-144">При указании параметра *PathName* заменяются параметры *ComputerName* и *QueueName*.</span><span class="sxs-lookup"><span data-stu-id="eafab-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="eafab-145">Конкретный параметр *FormatName* удаляет предыдущие сведения о параметре *ComputerName*, *QueueName* и *PathName* .</span><span class="sxs-lookup"><span data-stu-id="eafab-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="eafab-146">Связывание прослушивателя очередей компонентов с определенной частной очередью</span><span class="sxs-lookup"><span data-stu-id="eafab-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="eafab-147">Прослушиватель очередей компонентов COM+ получает только из очередей, связанных с приложением COM+, отмеченным как поставленное в очередь.</span><span class="sxs-lookup"><span data-stu-id="eafab-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="eafab-148">Если приложение COM+ помечается как поставленное в очередь, COM+ создает очередь сообщений, имя которой совпадает с именем приложения.</span><span class="sxs-lookup"><span data-stu-id="eafab-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="eafab-149">Имя формата очереди сообщений в этой очереди находится в каталоге COM+, связанном с приложением COM+.</span><span class="sxs-lookup"><span data-stu-id="eafab-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="eafab-150">Когда приложение COM+ запускается и помечается как Listen, запускается прослушиватель в процессе приложения COM+ и открывается очередь.</span><span class="sxs-lookup"><span data-stu-id="eafab-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="eafab-151">В следующей таблице перечислены параметры моникера очереди, влияющие на сообщение очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eafab-152">Параметр</span><span class="sxs-lookup"><span data-stu-id="eafab-152">Parameter</span></span></th>
<th><span data-ttu-id="eafab-153">Описание</span><span class="sxs-lookup"><span data-stu-id="eafab-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eafab-154"><em>Дл</em></span><span class="sxs-lookup"><span data-stu-id="eafab-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="eafab-155">Задает целое число без знака, например, с определяемым значением 12345.</span><span class="sxs-lookup"><span data-stu-id="eafab-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="eafab-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="eafab-157">Задает уровень проверки подлинности сообщения.</span><span class="sxs-lookup"><span data-stu-id="eafab-157">Specifies the message authentication level.</span></span> <span data-ttu-id="eafab-158">Сообщение с проверкой подлинности имеет цифровую подпись и требует сертификат для пользователя, отправляющего сообщение.</span><span class="sxs-lookup"><span data-stu-id="eafab-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="eafab-159">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="eafab-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="eafab-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-162"><em>Доставка</em></span><span class="sxs-lookup"><span data-stu-id="eafab-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="eafab-163">Указывает параметр доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="eafab-163">Specifies the message delivery option.</span></span> <span data-ttu-id="eafab-164">Это значение игнорируется для транзакционных очередей.</span><span class="sxs-lookup"><span data-stu-id="eafab-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="eafab-165">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="eafab-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="eafab-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-168"><em>енкрипталгорисм</em></span><span class="sxs-lookup"><span data-stu-id="eafab-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="eafab-169">Указывает алгоритм шифрования, используемый очередью сообщений для шифрования и расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="eafab-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="eafab-170">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-171">CALG_RC2, CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="eafab-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="eafab-172">Любое целочисленное значение, допустимое для очереди сообщений для <em>енкрипталгорисм</em>.</span><span class="sxs-lookup"><span data-stu-id="eafab-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="eafab-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="eafab-174">Задает криптографическую хэш-функцию.</span><span class="sxs-lookup"><span data-stu-id="eafab-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="eafab-175">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="eafab-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="eafab-177">Любое целочисленное значение, допустимое для очереди сообщений для <em>HashAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="eafab-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-178">Журнал</span><span class="sxs-lookup"><span data-stu-id="eafab-178">Journal</span></span><br/></td>
<td><span data-ttu-id="eafab-179">Указывает параметр журнала сообщений очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="eafab-180">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="eafab-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="eafab-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="eafab-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="eafab-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-184"><em>Label</em></span><span class="sxs-lookup"><span data-stu-id="eafab-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="eafab-185">Задает строку метки сообщения до MQ_MAX_MSG_LABEL_LEN символов.</span><span class="sxs-lookup"><span data-stu-id="eafab-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-186"><em>макстиметореачкуеуе</em></span><span class="sxs-lookup"><span data-stu-id="eafab-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="eafab-187">Указывает максимальное время (в секундах), в течение которого сообщение будет достигнуто в очереди.</span><span class="sxs-lookup"><span data-stu-id="eafab-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="eafab-188">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="eafab-189">INFINITE</span></span></li>
<li><span data-ttu-id="eafab-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="eafab-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="eafab-191">Количество секунд</span><span class="sxs-lookup"><span data-stu-id="eafab-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-192"><em>макстиметорецеиве</em></span><span class="sxs-lookup"><span data-stu-id="eafab-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="eafab-193">Указывает максимальное время (в секундах), в течение которого сообщение должно быть получено целевым приложением.</span><span class="sxs-lookup"><span data-stu-id="eafab-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="eafab-194">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="eafab-195">INFINITE</span></span></li>
<li><span data-ttu-id="eafab-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="eafab-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="eafab-197">Количество секунд</span><span class="sxs-lookup"><span data-stu-id="eafab-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-198"><em>Приоритет</em></span><span class="sxs-lookup"><span data-stu-id="eafab-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="eafab-199">Задает уровень приоритета сообщения в разрешенных значениях очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="eafab-200">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="eafab-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="eafab-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="eafab-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="eafab-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="eafab-204">Число от 0 до 7</span><span class="sxs-lookup"><span data-stu-id="eafab-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eafab-205"><em>привлевел</em></span><span class="sxs-lookup"><span data-stu-id="eafab-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="eafab-206">Задает уровень конфиденциальности, используемый для шифрования сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="eafab-207">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-208">MQMSG_PRIV_LEVEL_NONE, НЕТ, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="eafab-209">MQMSG_PRIV_LEVEL_BODY, ТЕКСТ,</span><span class="sxs-lookup"><span data-stu-id="eafab-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="eafab-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="eafab-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="eafab-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="eafab-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eafab-212"><em>Трассировка</em></span><span class="sxs-lookup"><span data-stu-id="eafab-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="eafab-213">Задает параметры трассировки, используемые при трассировке маршрутизации очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="eafab-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="eafab-214">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eafab-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="eafab-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="eafab-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="eafab-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="eafab-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eafab-217">Полный набор функций административного пакета SDK для COM+ доступен с помощью COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="eafab-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="eafab-218">Это позволяет любой программе запускать и прекращать работу приложений COM+ по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="eafab-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="eafab-219">При запуске приложения COM+ это приложение, которое выполняется, а не отдельные компоненты в приложении.</span><span class="sxs-lookup"><span data-stu-id="eafab-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="eafab-220">Если приложение вызывает компонент, не относящийся к очереди, запускается приложение COM+, содержащее компонент.</span><span class="sxs-lookup"><span data-stu-id="eafab-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="eafab-221">Если флажок прослушиватель включен, прослушиватель также запускается и начинает обработку сообщений для компонентов в очереди.</span><span class="sxs-lookup"><span data-stu-id="eafab-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="eafab-222">Несмотря на то, что служба очередей компонентов может запускаться таким образом, если компоненты, помещенные в очередь и не поставленные в очередь, упаковывались в одно приложение COM+, следует убедиться, что при выполнении компонента, не относящегося к очереди, должны запускаться компоненты из очереди.</span><span class="sxs-lookup"><span data-stu-id="eafab-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="eafab-223">Если это не так, упакуйте компоненты, помещенные в очередь, в приложение COM+, отдельное от других компонентов.</span><span class="sxs-lookup"><span data-stu-id="eafab-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eafab-224">См. также</span><span class="sxs-lookup"><span data-stu-id="eafab-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eafab-225">Активация очередей компонентов</span><span class="sxs-lookup"><span data-stu-id="eafab-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




