---
description: Извлекает битовую маску, определяющую наборы продуктов, доступные в системе. Если эта функция вызывается в приложении, которое выполняется в контексте сервера-приемника, вместо этого извлекается маска набора для приемника сервера.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Функция Ртлжетсуитемаск (Нтддк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663877"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="5b136-104">Функция Ртлжетсуитемаск</span><span class="sxs-lookup"><span data-stu-id="5b136-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="5b136-105">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5b136-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5b136-106">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5b136-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5b136-107">Извлекает битовую маску, определяющую наборы продуктов, доступные в системе.</span><span class="sxs-lookup"><span data-stu-id="5b136-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="5b136-108">Если эта функция вызывается в приложении, которое выполняется в контексте сервера-приемника, вместо этого извлекается маска набора для приемника сервера.</span><span class="sxs-lookup"><span data-stu-id="5b136-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b136-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b136-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="5b136-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b136-110">Parameters</span></span>

<span data-ttu-id="5b136-111">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="5b136-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b136-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b136-112">Return value</span></span>

<span data-ttu-id="5b136-113">Битовая маска, определяющая наборы продуктов, доступные в системе.</span><span class="sxs-lookup"><span data-stu-id="5b136-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="5b136-114">Битовая маска может включать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="5b136-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="5b136-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b136-115">Return value</span></span>                                                                          | <span data-ttu-id="5b136-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5b136-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5b136-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5b136-118">Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="5b136-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="5b136-119">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5b136-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5b136-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="5b136-121">Установлена операционная система Windows 10 Корпоративная, Windows 8.1 Enterprise, Windows Server 2008 Корпоративная, Windows Server 2003, Enterprise Edition или Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="5b136-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="5b136-122">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5b136-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="5b136-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="5b136-124">Компоненты Microsoft BackOffice установлены.</span><span class="sxs-lookup"><span data-stu-id="5b136-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="5b136-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="5b136-126">Установлен коммуникационный сервер 2003, коммуникационный сервер 2005, Communications Server 2007 или Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="5b136-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="5b136-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="5b136-128">Службы терминалов установлены.</span><span class="sxs-lookup"><span data-stu-id="5b136-128">Terminal Services is installed.</span></span> <span data-ttu-id="5b136-129">Это значение всегда задано.</span><span class="sxs-lookup"><span data-stu-id="5b136-129">This value is always set.</span></span><br/> <span data-ttu-id="5b136-130">Если параметр **терминалсервер** установлен, но параметр **синглеусертс** не установлен, система работает в режиме сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="5b136-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5b136-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="5b136-132">Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно.</span><span class="sxs-lookup"><span data-stu-id="5b136-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="5b136-133">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="5b136-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="5b136-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="5b136-135">Установлена операционная система Windows XP Embedded.</span><span class="sxs-lookup"><span data-stu-id="5b136-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="5b136-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="5b136-137">Установлен Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition или Windows 2000 Datacenter Server.</span><span class="sxs-lookup"><span data-stu-id="5b136-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="5b136-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="5b136-139">Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс.</span><span class="sxs-lookup"><span data-stu-id="5b136-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="5b136-140">Это значение задается, если система не работает в режиме сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="5b136-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="5b136-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="5b136-142">Установлена ОС Windows Vista Home Premium, Windows Vista Домашняя базовая или Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="5b136-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="5b136-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="5b136-144">Установлен выпуск Windows Server 2003, Web Edition.</span><span class="sxs-lookup"><span data-stu-id="5b136-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="5b136-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="5b136-146">Установлен Windows Storage Server 2003 R2 или Windows Storage Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5b136-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="5b136-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="5b136-148">Windows Server 2003, выпуски Compute Cluster Edition установлены.</span><span class="sxs-lookup"><span data-stu-id="5b136-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="5b136-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="5b136-150">Установлен Windows Home Server.</span><span class="sxs-lookup"><span data-stu-id="5b136-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="5b136-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b136-151">Remarks</span></span>

<span data-ttu-id="5b136-152">Не следует полагаться только на флаг 0x00000001, чтобы определить, установлен ли в системе малый бизнес-сервер, так как этот флаг и параметр 0x00000020 устанавливаются при установке этого набора продуктов.</span><span class="sxs-lookup"><span data-stu-id="5b136-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="5b136-153">Если вы обновите эту установку до Windows Server Standard Edition, флаг 0x00000020 будет сброшен, однако флаг 0x00000001 останется установленным.</span><span class="sxs-lookup"><span data-stu-id="5b136-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="5b136-154">В этом случае это означает, что в системе был установлен Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="5b136-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="5b136-155">Если эта установка будет обновлена до Windows Server, Enterprise Edition, флаг 0x00000001 останется установленным.</span><span class="sxs-lookup"><span data-stu-id="5b136-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b136-156">Требования</span><span class="sxs-lookup"><span data-stu-id="5b136-156">Requirements</span></span>



| <span data-ttu-id="5b136-157">Требование</span><span class="sxs-lookup"><span data-stu-id="5b136-157">Requirement</span></span> | <span data-ttu-id="5b136-158">Значение</span><span class="sxs-lookup"><span data-stu-id="5b136-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b136-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b136-159">Minimum supported client</span></span><br/> | <span data-ttu-id="5b136-160">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5b136-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5b136-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b136-161">Minimum supported server</span></span><br/> | <span data-ttu-id="5b136-162">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="5b136-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b136-163">Header</span><span class="sxs-lookup"><span data-stu-id="5b136-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b136-164"><dt>Нтддк. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b136-165">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b136-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b136-166"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b136-167">DLL</span><span class="sxs-lookup"><span data-stu-id="5b136-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b136-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b136-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




