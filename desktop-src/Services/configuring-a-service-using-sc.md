---
description: Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для запроса или изменения базы данных установленных служб. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Настройка службы с помощью SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662254"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="fde5a-105">Настройка службы с помощью SC</span><span class="sxs-lookup"><span data-stu-id="fde5a-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="fde5a-106">Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для запроса или изменения базы данных установленных служб.</span><span class="sxs-lookup"><span data-stu-id="fde5a-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="fde5a-107">Его команды соответствуют функциям, предоставляемым SCM.</span><span class="sxs-lookup"><span data-stu-id="fde5a-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="fde5a-108">Синтаксис выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="fde5a-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde5a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fde5a-109">Syntax</span></span>

<span data-ttu-id="fde5a-110">**SC** \[ *Имя сервера* \] *Команда* \[  \] ServiceName \[  \] параметр1 \[ *параметр2* \] ...</span><span class="sxs-lookup"><span data-stu-id="fde5a-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="fde5a-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Имя*</span><span class="sxs-lookup"><span data-stu-id="fde5a-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="fde5a-112">Необязательное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fde5a-112">Optional server name.</span></span> <span data-ttu-id="fde5a-113">Используйте форму \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="fde5a-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="fde5a-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Кнопки*</span><span class="sxs-lookup"><span data-stu-id="fde5a-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="fde5a-115">Одна из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="fde5a-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="fde5a-116">boot</span><span class="sxs-lookup"><span data-stu-id="fde5a-116">boot</span></span></dd> <dd><span data-ttu-id="fde5a-117">config</span><span class="sxs-lookup"><span data-stu-id="fde5a-117">config</span></span></dd> <dd><span data-ttu-id="fde5a-118">create</span><span class="sxs-lookup"><span data-stu-id="fde5a-118">create</span></span></dd> <dd><span data-ttu-id="fde5a-119">удалить</span><span class="sxs-lookup"><span data-stu-id="fde5a-119">delete</span></span></dd> <dd><span data-ttu-id="fde5a-120">description;</span><span class="sxs-lookup"><span data-stu-id="fde5a-120">description</span></span></dd> <dd><span data-ttu-id="fde5a-121">енумдепенд</span><span class="sxs-lookup"><span data-stu-id="fde5a-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="fde5a-122">ошибка</span><span class="sxs-lookup"><span data-stu-id="fde5a-122">failure</span></span></dd> <dd><span data-ttu-id="fde5a-123">фаилурефлаг</span><span class="sxs-lookup"><span data-stu-id="fde5a-123">failureflag</span></span></dd> <dd><span data-ttu-id="fde5a-124">Переdisplayname</span><span class="sxs-lookup"><span data-stu-id="fde5a-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="fde5a-125">жеткэйнаме</span><span class="sxs-lookup"><span data-stu-id="fde5a-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="fde5a-126">Блокировка</span><span class="sxs-lookup"><span data-stu-id="fde5a-126">Lock</span></span></dd> <dd><span data-ttu-id="fde5a-127">qc</span><span class="sxs-lookup"><span data-stu-id="fde5a-127">qc</span></span></dd> <dd><span data-ttu-id="fde5a-128">кдескриптион</span><span class="sxs-lookup"><span data-stu-id="fde5a-128">qdescription</span></span></dd> <dd><span data-ttu-id="fde5a-129">кфаилуре</span><span class="sxs-lookup"><span data-stu-id="fde5a-129">qfailure</span></span></dd> <dd><span data-ttu-id="fde5a-130">кфаилурефлаг</span><span class="sxs-lookup"><span data-stu-id="fde5a-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="fde5a-131">кпривс</span><span class="sxs-lookup"><span data-stu-id="fde5a-131">qprivs</span></span></dd> <dd><span data-ttu-id="fde5a-132">ксидтипе</span><span class="sxs-lookup"><span data-stu-id="fde5a-132">qsidtype</span></span></dd> <dd><span data-ttu-id="fde5a-133">query</span><span class="sxs-lookup"><span data-stu-id="fde5a-133">query</span></span></dd> <dd><span data-ttu-id="fde5a-134">QueryEx</span><span class="sxs-lookup"><span data-stu-id="fde5a-134">queryex</span></span></dd> <dd><span data-ttu-id="fde5a-135">привс</span><span class="sxs-lookup"><span data-stu-id="fde5a-135">privs</span></span></dd> <dd><span data-ttu-id="fde5a-136">куерилокк</span><span class="sxs-lookup"><span data-stu-id="fde5a-136">QueryLock</span></span></dd> <dd><span data-ttu-id="fde5a-137">sdset</span><span class="sxs-lookup"><span data-stu-id="fde5a-137">sdset</span></span></dd> <dd><span data-ttu-id="fde5a-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="fde5a-138">sdshow</span></span></dd> <dd><span data-ttu-id="fde5a-139">showsid</span><span class="sxs-lookup"><span data-stu-id="fde5a-139">showsid</span></span></dd> <dd><span data-ttu-id="fde5a-140">Идентификатор типа безопасности</span><span class="sxs-lookup"><span data-stu-id="fde5a-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="fde5a-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Служба*</span><span class="sxs-lookup"><span data-stu-id="fde5a-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="fde5a-142">Имя службы, указанное при ее установке.</span><span class="sxs-lookup"><span data-stu-id="fde5a-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="fde5a-143"><span id="option1"></span><span id="OPTION1"></span>*параметр1*</span><span class="sxs-lookup"><span data-stu-id="fde5a-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="fde5a-144">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="fde5a-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fde5a-145"><span id="option2"></span><span id="OPTION2"></span>*вариант 2*</span><span class="sxs-lookup"><span data-stu-id="fde5a-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="fde5a-146">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="fde5a-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fde5a-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fde5a-147">Remarks</span></span>

<span data-ttu-id="fde5a-148">Чтобы просмотреть полный синтаксис команды, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fde5a-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="fde5a-149"> *команда* SC</span><span class="sxs-lookup"><span data-stu-id="fde5a-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="fde5a-150">См. также</span><span class="sxs-lookup"><span data-stu-id="fde5a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde5a-151">Конфигурация службы</span><span class="sxs-lookup"><span data-stu-id="fde5a-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="fde5a-152">Установка, удаление и перечисление служб</span><span class="sxs-lookup"><span data-stu-id="fde5a-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



