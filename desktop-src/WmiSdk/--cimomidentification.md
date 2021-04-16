---
description: Описывает локальную установку WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Класс __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702511"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="c1197-103">\_\_Класс Цимомидентификатион</span><span class="sxs-lookup"><span data-stu-id="c1197-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="c1197-104">Системный класс **\_ \_ Цимомидентификатион** описывает локальную установку WMI.</span><span class="sxs-lookup"><span data-stu-id="c1197-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="c1197-105">Это одноэлементный класс; Существует только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="c1197-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="c1197-106">Класс **\_ \_ Цимомидентификатион** доступен только в **корневых** и корневых пространствах имен **\\ по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="c1197-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="c1197-107">Пользователи запрашивают экземпляр для получения сведений об установке WMI.</span><span class="sxs-lookup"><span data-stu-id="c1197-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="c1197-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c1197-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c1197-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c1197-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1197-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1197-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="c1197-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c1197-111">Members</span></span>

<span data-ttu-id="c1197-112">Класс **\_ \_ Цимомидентификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c1197-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="c1197-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1197-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1197-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c1197-114">Properties</span></span>

<span data-ttu-id="c1197-115">Класс **\_ \_ Цимомидентификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c1197-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c1197-116">**сетупдатетиме**</span><span class="sxs-lookup"><span data-stu-id="c1197-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1197-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1197-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1197-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1197-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1197-119">Дата и время установки.</span><span class="sxs-lookup"><span data-stu-id="c1197-119">Date and time of installation.</span></span> <span data-ttu-id="c1197-120">Это свойство пусто после установки операционной системы в первый раз.</span><span class="sxs-lookup"><span data-stu-id="c1197-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="c1197-121">Если репозиторий WMI был удален, а затем создан снова, это свойство содержит дату и время повторного создания репозитория.</span><span class="sxs-lookup"><span data-stu-id="c1197-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="c1197-122">**версионкуррентлируннинг**</span><span class="sxs-lookup"><span data-stu-id="c1197-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1197-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1197-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1197-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1197-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1197-125">Указывает версию фактического образа, содержащего службу WMI, которая создала репозиторий модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="c1197-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="c1197-126">Так как формат репозитория может измениться между версиями WMI, это свойство позволяет будущим обновлениям WMI определить, нужно ли обновить базу данных.</span><span class="sxs-lookup"><span data-stu-id="c1197-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="c1197-127">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="c1197-127">The format is:</span></span>

<span data-ttu-id="c1197-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="c1197-128">"1.00.183.0000"</span></span>

<span data-ttu-id="c1197-129">Если первая цифра является основной версией, следующие две цифры являются дополнительными версиями, а следующие три цифры — номером сборки.</span><span class="sxs-lookup"><span data-stu-id="c1197-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="c1197-130">Остальные цифры не используются.</span><span class="sxs-lookup"><span data-stu-id="c1197-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1197-131">**версионуседтокреатедб**</span><span class="sxs-lookup"><span data-stu-id="c1197-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1197-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1197-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1197-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1197-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1197-134">Указывает версию фактического образа, содержащего службу WMI, которая создала репозиторий CIM.</span><span class="sxs-lookup"><span data-stu-id="c1197-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="c1197-135">Так как формат репозитория может измениться между версиями WMI, это свойство позволяет будущим обновлениям WMI определить, нужно ли обновить базу данных.</span><span class="sxs-lookup"><span data-stu-id="c1197-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="c1197-136">Формат будет следующим:</span><span class="sxs-lookup"><span data-stu-id="c1197-136">The format is:</span></span>

<span data-ttu-id="c1197-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="c1197-137">"1.00.183.0000"</span></span>

<span data-ttu-id="c1197-138">Если первая цифра является основной версией, следующие две цифры являются дополнительными версиями, а следующие три цифры — номером сборки.</span><span class="sxs-lookup"><span data-stu-id="c1197-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="c1197-139">Остальные цифры не используются.</span><span class="sxs-lookup"><span data-stu-id="c1197-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1197-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="c1197-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1197-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c1197-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c1197-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c1197-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c1197-143">Каталог установки.</span><span class="sxs-lookup"><span data-stu-id="c1197-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1197-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1197-144">Remarks</span></span>

<span data-ttu-id="c1197-145">Класс **\_ \_ Цимомидентификатион** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="c1197-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="c1197-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1197-146">Examples</span></span>

<span data-ttu-id="c1197-147">В следующем образце кода VBScript описывается, как отобразить сведения об идентификации объектной модели CIM и они были взяты из каталога примеров в папке \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ сисмгмт \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="c1197-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="c1197-148">В следующем образце кода Perl описывается, как отобразить сведения об идентификации объектной модели CIM и они были взяты из каталога примеров в папке \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ сисмгмт \\ WMI \\ scripting.</span><span class="sxs-lookup"><span data-stu-id="c1197-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="c1197-149">Требования</span><span class="sxs-lookup"><span data-stu-id="c1197-149">Requirements</span></span>



| <span data-ttu-id="c1197-150">Требование</span><span class="sxs-lookup"><span data-stu-id="c1197-150">Requirement</span></span> | <span data-ttu-id="c1197-151">Значение</span><span class="sxs-lookup"><span data-stu-id="c1197-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c1197-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1197-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c1197-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1197-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c1197-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1197-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c1197-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1197-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c1197-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1197-156">Namespace</span></span><br/>                | <span data-ttu-id="c1197-157">Root</span><span class="sxs-lookup"><span data-stu-id="c1197-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c1197-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1197-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1197-159">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="c1197-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="c1197-160">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="c1197-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

