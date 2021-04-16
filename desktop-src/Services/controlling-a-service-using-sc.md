---
description: Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для управления службой. Его команды соответствуют функциям, предоставляемым SCM. Синтаксис выглядит следующим образом.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Управление службой с помощью SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664201"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="1ea90-105">Управление службой с помощью SC</span><span class="sxs-lookup"><span data-stu-id="1ea90-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="1ea90-106">Windows SDK содержит служебную программу командной строки Sc.exe, которая может использоваться для управления службой.</span><span class="sxs-lookup"><span data-stu-id="1ea90-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="1ea90-107">Его команды соответствуют функциям, предоставляемым SCM.</span><span class="sxs-lookup"><span data-stu-id="1ea90-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="1ea90-108">Синтаксис выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="1ea90-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea90-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ea90-109">Syntax</span></span>

<span data-ttu-id="1ea90-110">**SC** \[ *Имя сервера* \] *Команда* \[  \] ServiceName \[  \] параметр1 \[ *параметр2* \] ...</span><span class="sxs-lookup"><span data-stu-id="1ea90-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="1ea90-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Имя*</span><span class="sxs-lookup"><span data-stu-id="1ea90-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="1ea90-112">Необязательное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1ea90-112">Optional server name.</span></span> <span data-ttu-id="1ea90-113">Используйте форму \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="1ea90-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="1ea90-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Кнопки*</span><span class="sxs-lookup"><span data-stu-id="1ea90-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="1ea90-115">Одна из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="1ea90-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="1ea90-116">continue</span><span class="sxs-lookup"><span data-stu-id="1ea90-116">continue</span></span></dd> <dd><span data-ttu-id="1ea90-117">управляющие</span><span class="sxs-lookup"><span data-stu-id="1ea90-117">control</span></span></dd> <dd><span data-ttu-id="1ea90-118">запросить</span><span class="sxs-lookup"><span data-stu-id="1ea90-118">interrogate</span></span></dd> <dd><span data-ttu-id="1ea90-119">pause</span><span class="sxs-lookup"><span data-stu-id="1ea90-119">pause</span></span></dd> <dd><span data-ttu-id="1ea90-120">start</span><span class="sxs-lookup"><span data-stu-id="1ea90-120">start</span></span></dd> <dd><span data-ttu-id="1ea90-121">stop</span><span class="sxs-lookup"><span data-stu-id="1ea90-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="1ea90-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Служба*</span><span class="sxs-lookup"><span data-stu-id="1ea90-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="1ea90-123">Имя службы, указанное при ее установке.</span><span class="sxs-lookup"><span data-stu-id="1ea90-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="1ea90-124"><span id="option1"></span><span id="OPTION1"></span>*параметр1*</span><span class="sxs-lookup"><span data-stu-id="1ea90-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="1ea90-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="1ea90-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1ea90-126"><span id="option2"></span><span id="OPTION2"></span>*вариант 2*</span><span class="sxs-lookup"><span data-stu-id="1ea90-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="1ea90-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="1ea90-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ea90-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ea90-128">Remarks</span></span>

<span data-ttu-id="1ea90-129">Чтобы просмотреть полный синтаксис команды, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1ea90-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="1ea90-130"> *команда* SC</span><span class="sxs-lookup"><span data-stu-id="1ea90-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea90-131">См. также</span><span class="sxs-lookup"><span data-stu-id="1ea90-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea90-132">Запросы управления службами</span><span class="sxs-lookup"><span data-stu-id="1ea90-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="1ea90-133">Запуск службы</span><span class="sxs-lookup"><span data-stu-id="1ea90-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



