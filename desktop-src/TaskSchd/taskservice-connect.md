---
title: TaskService. Connect, метод
description: Для создания сценариев подключается к удаленному компьютеру и связывает все последующие вызовы в этом интерфейсе с удаленным сеансом.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Метод Connect планировщик задач
- Метод Connect планировщик задач, объект TaskService
- Планировщик задач объекта TaskService, метод Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988418"
---
# <a name="taskserviceconnect-method"></a><span data-ttu-id="364d9-106">TaskService. Connect, метод</span><span class="sxs-lookup"><span data-stu-id="364d9-106">TaskService.Connect method</span></span>

<span data-ttu-id="364d9-107">Для создания сценариев подключается к удаленному компьютеру и связывает все последующие вызовы в этом интерфейсе с удаленным сеансом.</span><span class="sxs-lookup"><span data-stu-id="364d9-107">For scripting, connects to a remote machine and associates all subsequent calls on this interface with a remote session.</span></span> <span data-ttu-id="364d9-108">Если параметр serverName пуст, то этот метод будет выполняться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="364d9-108">If the serverName parameter is empty, then this method will execute on the local computer.</span></span> <span data-ttu-id="364d9-109">Если userId не указан, используется текущий токен.</span><span class="sxs-lookup"><span data-stu-id="364d9-109">If the userId is not specified, then the current token is used.</span></span>

## <a name="syntax"></a><span data-ttu-id="364d9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="364d9-110">Syntax</span></span>


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a><span data-ttu-id="364d9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="364d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="364d9-112">*имя сервера* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="364d9-112">*serverName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="364d9-113">Имя компьютера, к которому необходимо подключиться.</span><span class="sxs-lookup"><span data-stu-id="364d9-113">The name of the computer that you want to connect to.</span></span> <span data-ttu-id="364d9-114">Если параметр serverName пуст, то этот метод будет выполняться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="364d9-114">If the serverName parameter is empty, then this method will execute on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="364d9-115">*пользователь* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="364d9-115">*user* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="364d9-116">Имя пользователя, используемое во время подключения к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="364d9-116">The user name that is used during the connection to the computer.</span></span> <span data-ttu-id="364d9-117">Если пользователь не указан, используется текущий токен.</span><span class="sxs-lookup"><span data-stu-id="364d9-117">If the user is not specified, then the current token is used.</span></span>

</dd> <dt>

<span data-ttu-id="364d9-118">*домен* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="364d9-118">*domain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="364d9-119">Домен пользователя, указанный в параметре *User* .</span><span class="sxs-lookup"><span data-stu-id="364d9-119">The domain of the user specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="364d9-120">*пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="364d9-120">*password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="364d9-121">Пароль, используемый для подключения к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="364d9-121">The password that is used to connect to the computer.</span></span> <span data-ttu-id="364d9-122">Если имя пользователя и пароль не указаны, используется текущий токен.</span><span class="sxs-lookup"><span data-stu-id="364d9-122">If the user name and password are not specified, then the current token is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="364d9-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="364d9-123">Return value</span></span>

<span data-ttu-id="364d9-124">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="364d9-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="364d9-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="364d9-125">Remarks</span></span>

<span data-ttu-id="364d9-126">Метод **TaskService. Connect** следует вызывать до вызова любого из других методов [**TaskService**](taskservice.md) .</span><span class="sxs-lookup"><span data-stu-id="364d9-126">The **TaskService.Connect** method should be called before calling any of the other [**TaskService**](taskservice.md) methods.</span></span>

<span data-ttu-id="364d9-127">Если метод Connect завершается неудачей, можно получить Идентификатор ошибки, чтобы найти значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="364d9-127">If the Connect method fails, you can collect the error identifier to find the meaning of the error.</span></span> <span data-ttu-id="364d9-128">В следующей таблице перечислены идентификаторы ошибок и их описания.</span><span class="sxs-lookup"><span data-stu-id="364d9-128">The following table lists the error identifiers and their descriptions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="364d9-129">Идентификатор ошибки</span><span class="sxs-lookup"><span data-stu-id="364d9-129">Error Identifier</span></span></th>
<th><span data-ttu-id="364d9-130">Описание</span><span class="sxs-lookup"><span data-stu-id="364d9-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="364d9-131">0x80070005</span><span class="sxs-lookup"><span data-stu-id="364d9-131">0x80070005</span></span></td>
<td><span data-ttu-id="364d9-132">Отказано в доступе для подключения к службе планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="364d9-132">Access is denied to connect to the Task Scheduler service.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="364d9-133">0x80041315</span><span class="sxs-lookup"><span data-stu-id="364d9-133">0x80041315</span></span></td>
<td><span data-ttu-id="364d9-134">Служба планировщик задач не запущена.</span><span class="sxs-lookup"><span data-stu-id="364d9-134">The Task Scheduler service is not running.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="364d9-135">0x8007000e</span><span class="sxs-lookup"><span data-stu-id="364d9-135">0x8007000e</span></span></td>
<td><span data-ttu-id="364d9-136">Приложению не хватает памяти для выполнения операции, или <em>пользователь</em>, <em>пароль</em>или <em>домен</em> имеют по крайней мере одно значение NULL и одно из значений, отличных от NULL.</span><span class="sxs-lookup"><span data-stu-id="364d9-136">The application does not have enough memory to complete the operation or the <em>user</em>, <em>password</em>, or <em>domain</em> has at least one null and one non-null value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="364d9-137">53</span><span class="sxs-lookup"><span data-stu-id="364d9-137">53</span></span></td>
<td><span data-ttu-id="364d9-138">Эта ошибка возвращается в следующих ситуациях.</span><span class="sxs-lookup"><span data-stu-id="364d9-138">This error is returned in the following situations:</span></span>
<ul>
<li><span data-ttu-id="364d9-139">Имя компьютера, указанное в параметре <em>ServerName</em> , не существует.</span><span class="sxs-lookup"><span data-stu-id="364d9-139">The computer name specified in the <em>serverName</em> parameter does not exist.</span></span></li>
<li><span data-ttu-id="364d9-140">При попытке подключиться к компьютеру под управлением Windows Server 2003 или Windows XP на удаленном компьютере не включено исключение брандмауэра для общего доступа к файлам и принтерам, или служба удаленного реестра не запущена.</span><span class="sxs-lookup"><span data-stu-id="364d9-140">When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</span></span></li>
<li><span data-ttu-id="364d9-141">При попытке подключиться к компьютеру под управлением Windows Vista на удаленном компьютере не включено исключение брандмауэра Управление удаленными задачами и отключено исключение брандмауэра для общего доступа к файлам и принтерам, либо служба удаленного реестра не запущена.</span><span class="sxs-lookup"><span data-stu-id="364d9-141">When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="364d9-142">50</span><span class="sxs-lookup"><span data-stu-id="364d9-142">50</span></span></td>
<td><span data-ttu-id="364d9-143">Параметры <em>пользователя</em>, <em>пароля</em>или <em>домена</em> не могут быть указаны при подключении к удаленному компьютеру Windows XP или Windows Server 2003 с компьютера под управлением Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="364d9-143">The <em>user</em>, <em>password</em>, or <em>domain</em> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="364d9-144">При подключении к удаленному компьютеру с ОС Windows Vista из Windows Vista необходимо разрешить удаленное исключение для удаленного управления назначенными задачами на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="364d9-144">If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer.</span></span> <span data-ttu-id="364d9-145">Чтобы разрешить это исключение, нажмите кнопку Пуск, панель управления, безопасность, разрешить программу через брандмауэр Windows, а затем установите флажок Удаленное управление назначенными задачами.</span><span class="sxs-lookup"><span data-stu-id="364d9-145">To allow this exception click Start, Control Panel, Security, Allow a program through Windows Firewall, and then select the Remote Scheduled Tasks Management check box.</span></span> <span data-ttu-id="364d9-146">Затем нажмите кнопку ОК в диалоговом окне Параметры брандмауэра Windows.</span><span class="sxs-lookup"><span data-stu-id="364d9-146">Then click the Ok button in the Windows Firewall Settings dialog box.</span></span>

<span data-ttu-id="364d9-147">При подключении к удаленному компьютеру Windows XP или Windows Server 2003 с компьютера под управлением Windows Vista необходимо разрешить исключение брандмауэра для общего доступа к файлам и принтерам на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="364d9-147">If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer.</span></span> <span data-ttu-id="364d9-148">Чтобы разрешить это исключение, нажмите кнопку Пуск, панель управления, дважды щелкните Брандмауэр Windows, перейдите на вкладку исключения и выберите исключение брандмауэра для общего доступа к файлам и принтерам.</span><span class="sxs-lookup"><span data-stu-id="364d9-148">To allow this exception click Start, Control Panel, double-click Windows Firewall, select the Exceptions tab, and then select the File and Printer Sharing firewall exception.</span></span> <span data-ttu-id="364d9-149">Затем нажмите кнопку ОК в диалоговом окне Брандмауэр Windows.</span><span class="sxs-lookup"><span data-stu-id="364d9-149">Then click the OK button in the Windows Firewall dialog box.</span></span> <span data-ttu-id="364d9-150">Служба удаленного реестра также должна быть запущена на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="364d9-150">The Remote Registry service must also be running on the remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="364d9-151">Требования</span><span class="sxs-lookup"><span data-stu-id="364d9-151">Requirements</span></span>



| <span data-ttu-id="364d9-152">Требование</span><span class="sxs-lookup"><span data-stu-id="364d9-152">Requirement</span></span> | <span data-ttu-id="364d9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="364d9-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="364d9-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="364d9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="364d9-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="364d9-155">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="364d9-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="364d9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="364d9-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="364d9-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="364d9-158">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="364d9-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="364d9-159"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="364d9-159"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="364d9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="364d9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="364d9-161"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="364d9-161"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





