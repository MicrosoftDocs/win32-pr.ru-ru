---
description: '&Win32 \_ привилежесстатус \# 8194; Класс WMI сообщает сведения о привилегиях, необходимых для выполнения операции. Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.'
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Класс Win32_PrivilegesStatus (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895937"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="9f141-104">Класс Win32_PrivilegesStatus (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9f141-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9f141-105"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ привилежесстатус для Win32** сообщает сведения о привилегиях, необходимых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9f141-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="9f141-106">Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9f141-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="9f141-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9f141-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9f141-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="9f141-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f141-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f141-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="9f141-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9f141-110">Members</span></span>

<span data-ttu-id="9f141-111">Класс **Win32 \_ привилежесстатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9f141-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="9f141-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f141-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f141-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f141-113">Properties</span></span>

<span data-ttu-id="9f141-114">Класс **Win32 \_ привилежесстатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f141-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f141-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f141-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f141-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f141-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f141-118">Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.</span><span class="sxs-lookup"><span data-stu-id="9f141-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="9f141-119">Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f141-120">**Операция**</span><span class="sxs-lookup"><span data-stu-id="9f141-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f141-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f141-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f141-123">Операция, выполняемая во время сбоя или аномалии.</span><span class="sxs-lookup"><span data-stu-id="9f141-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="9f141-124">Как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="9f141-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="9f141-125">Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f141-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="9f141-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f141-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f141-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f141-129">Параметры, участвующие в изменении состояния или ошибки.</span><span class="sxs-lookup"><span data-stu-id="9f141-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="9f141-130">Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f141-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="9f141-131">Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f141-132">**привилежесноселд**</span><span class="sxs-lookup"><span data-stu-id="9f141-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9f141-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f141-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f141-135">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")</span><span class="sxs-lookup"><span data-stu-id="9f141-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="9f141-136">Список необходимых привилегий доступа отсутствует для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9f141-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="9f141-137">Типы привилегий доступа можно найти в разделе "привилегии Windows".</span><span class="sxs-lookup"><span data-stu-id="9f141-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="9f141-138">Пример: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="9f141-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="9f141-139">**привилежесрекуиред**</span><span class="sxs-lookup"><span data-stu-id="9f141-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-140">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9f141-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f141-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f141-142">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")</span><span class="sxs-lookup"><span data-stu-id="9f141-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="9f141-143">Список всех привилегий, необходимых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9f141-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="9f141-144">К ним относятся значения из свойства **привилежесноселд** .</span><span class="sxs-lookup"><span data-stu-id="9f141-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="9f141-145">Пример: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="9f141-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="9f141-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="9f141-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f141-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f141-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f141-149">Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="9f141-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="9f141-150">Если поставщик не задействован, для этой строки задается значение "Управление Windows".</span><span class="sxs-lookup"><span data-stu-id="9f141-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="9f141-151">Это свойство наследуется от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f141-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="9f141-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f141-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f141-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f141-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f141-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f141-155">Содержит код ошибки или сведения для операции.</span><span class="sxs-lookup"><span data-stu-id="9f141-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="9f141-156">Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха.</span><span class="sxs-lookup"><span data-stu-id="9f141-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="9f141-157">Это свойство наследуется от [**\_ \_ нотифистатус**](../wmisdk/--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f141-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f141-158">Remarks</span></span>

<span data-ttu-id="9f141-159">Класс **Win32 \_ привилежесстатус** является производным от [**\_ \_ екстендедстатус**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9f141-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f141-160">Требования</span><span class="sxs-lookup"><span data-stu-id="9f141-160">Requirements</span></span>



| <span data-ttu-id="9f141-161">Требование</span><span class="sxs-lookup"><span data-stu-id="9f141-161">Requirement</span></span> | <span data-ttu-id="9f141-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9f141-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f141-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f141-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9f141-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f141-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f141-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f141-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9f141-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f141-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f141-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9f141-167">Namespace</span></span><br/>                | <span data-ttu-id="9f141-168">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9f141-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f141-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9f141-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f141-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f141-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f141-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9f141-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f141-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f141-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f141-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f141-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f141-174">**\_\_екстендедстатус**</span><span class="sxs-lookup"><span data-stu-id="9f141-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
