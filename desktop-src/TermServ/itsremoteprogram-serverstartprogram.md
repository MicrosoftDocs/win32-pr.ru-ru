---
title: Итсремотепрограм Серверстартпрограм, метод
description: Указывает программу RemoteApp для запуска в удаленном сеансе.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Серверстартпрограм
- Службы удаленных рабочих столов метода Серверстартпрограм, интерфейс Итсремотепрограм
- Службы удаленных рабочих столов интерфейса Итсремотепрограм, метод Серверстартпрограм
- Службы удаленных рабочих столов метода Серверстартпрограм, интерфейс ITSRemoteProgram2
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram2, метод Серверстартпрограм
- Службы удаленных рабочих столов метода Серверстартпрограм, интерфейс ITSRemoteProgram3
- Службы удаленных рабочих столов интерфейса ITSRemoteProgram3, метод Серверстартпрограм
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534430"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="3a4b2-110">Метод Итсремотепрограм:: Серверстартпрограм</span><span class="sxs-lookup"><span data-stu-id="3a4b2-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="3a4b2-111">Указывает программу RemoteApp для запуска в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="3a4b2-112">Эта функция должна вызываться для подключенного сеанса (после получения уведомления о подключении к сеансу на клиенте).</span><span class="sxs-lookup"><span data-stu-id="3a4b2-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="3a4b2-113">В сеансе можно запустить любое количество удаленных приложений RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="3a4b2-114">Время ожидания сеанса RemoteApp истечет, если в сеансе не будет запущено ни одной программы RemoteApp в течение времени ожидания, что составляет два минуты для Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4b2-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a4b2-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="3a4b2-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a4b2-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4b2-117">*бстрексекутаблепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-118">Путь к исполняемому файлу программы RemoteApp на сервере.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="3a4b2-119">*бстрфилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-120">Путь к файлу, открываемому на сервере с помощью сопоставления файлов, например "C: \\ \\ documents \\ \\MyReport.docx".</span><span class="sxs-lookup"><span data-stu-id="3a4b2-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="3a4b2-121">При указании *бстрфилепас* не следует указывать параметр *бстрексекутаблепас* и наоборот.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="3a4b2-122">Следует указать только один из параметров.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="3a4b2-123">*бстрворкингдиректори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-124">Рабочий каталог на сервере для программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="3a4b2-125">*вбекспанденвваринворкингдиректорйонсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-126">Указывает, должен ли сервер расширять переменные среды в пути к рабочему каталогу.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="3a4b2-127">Присвойте этому параметру значение **\_ true** , если путь к рабочему каталогу содержит переменные среды, или значение **\_ false** , если путь к рабочему каталогу не содержит переменных среды.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="3a4b2-128">*бстраргументс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-129">Аргументы командной строки для программы RemoteApp, указанные в *бстрексекутаблепас*.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="3a4b2-130">Установите значение **null** , если *бстрексекутаблепас* не указан.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="3a4b2-131">*вбекспанденвваринаргументсонсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a4b2-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4b2-132">Указывает, должен ли сервер расширять переменные среды в аргументах командной строки.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="3a4b2-133">Присвойте этому параметру значение **\_ true** , если аргументы содержат переменные среды, **или \_ значение false** , если аргументы не содержат переменных среды.</span><span class="sxs-lookup"><span data-stu-id="3a4b2-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4b2-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a4b2-134">Return value</span></span>

<span data-ttu-id="3a4b2-135">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="3a4b2-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4b2-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3a4b2-136">Requirements</span></span>



| <span data-ttu-id="3a4b2-137">Требование</span><span class="sxs-lookup"><span data-stu-id="3a4b2-137">Requirement</span></span> | <span data-ttu-id="3a4b2-138">Значение</span><span class="sxs-lookup"><span data-stu-id="3a4b2-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4b2-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a4b2-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4b2-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a4b2-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3a4b2-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a4b2-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4b2-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a4b2-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3a4b2-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3a4b2-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a4b2-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4b2-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a4b2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4b2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a4b2-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4b2-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a4b2-147">IID</span><span class="sxs-lookup"><span data-stu-id="3a4b2-147">IID</span></span><br/>                      | <span data-ttu-id="3a4b2-148">IID \_ итсремотепрограм определен как FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="3a4b2-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="3a4b2-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a4b2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4b2-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="3a4b2-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="3a4b2-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="3a4b2-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="3a4b2-152">**итсремотепрограм**</span><span class="sxs-lookup"><span data-stu-id="3a4b2-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





