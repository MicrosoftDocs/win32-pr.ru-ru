---
description: '&Win32 \_ привилежесстатус \# 8194; Класс WMI сообщает сведения о привилегиях, необходимых для выполнения операции. Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.'
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Класс Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272737"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="39ea2-104">Класс Win32_PrivilegesStatus (WMI)</span><span class="sxs-lookup"><span data-stu-id="39ea2-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="39ea2-105">[Класс WMI](retrieving-a-class.md) **\_ привилежесстатус для Win32** сообщает сведения о привилегиях, необходимых для выполнения операции.   </span><span class="sxs-lookup"><span data-stu-id="39ea2-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="39ea2-106">Он может быть возвращен при сбое операции или при возвращении частично заполненного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="39ea2-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="39ea2-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="39ea2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="39ea2-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="39ea2-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ea2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39ea2-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="39ea2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="39ea2-110">Members</span></span>

<span data-ttu-id="39ea2-111">Класс **Win32 \_ привилежесстатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39ea2-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="39ea2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="39ea2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39ea2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="39ea2-113">Properties</span></span>

<span data-ttu-id="39ea2-114">Класс **Win32 \_ привилежесстатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39ea2-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39ea2-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39ea2-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39ea2-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-118">Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.</span><span class="sxs-lookup"><span data-stu-id="39ea2-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="39ea2-119">Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-120">**Операция**</span><span class="sxs-lookup"><span data-stu-id="39ea2-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39ea2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-123">Операция, выполняемая во время сбоя или аномалии.</span><span class="sxs-lookup"><span data-stu-id="39ea2-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="39ea2-124">Как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="39ea2-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="39ea2-125">Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="39ea2-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39ea2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-129">Параметры, участвующие в изменении состояния или ошибки.</span><span class="sxs-lookup"><span data-stu-id="39ea2-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="39ea2-130">Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="39ea2-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="39ea2-131">Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-132">**привилежесноселд**</span><span class="sxs-lookup"><span data-stu-id="39ea2-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="39ea2-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-135">Список необходимых привилегий доступа отсутствует для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="39ea2-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="39ea2-136">Типы привилегий доступа можно найти в разделе "привилегии Windows".</span><span class="sxs-lookup"><span data-stu-id="39ea2-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="39ea2-137">Пример: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="39ea2-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-138">**привилежесрекуиред**</span><span class="sxs-lookup"><span data-stu-id="39ea2-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-139">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="39ea2-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-141">Список всех привилегий, необходимых для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="39ea2-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="39ea2-142">К ним относятся значения из свойства **привилежесноселд** .</span><span class="sxs-lookup"><span data-stu-id="39ea2-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="39ea2-143">Пример: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="39ea2-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="39ea2-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39ea2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-147">Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="39ea2-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="39ea2-148">Если поставщик не задействован, для этой строки задается значение "Управление Windows".</span><span class="sxs-lookup"><span data-stu-id="39ea2-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="39ea2-149">Это свойство наследуется от [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="39ea2-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="39ea2-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39ea2-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="39ea2-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39ea2-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39ea2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39ea2-153">Содержит код ошибки или сведения для операции.</span><span class="sxs-lookup"><span data-stu-id="39ea2-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="39ea2-154">Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха.</span><span class="sxs-lookup"><span data-stu-id="39ea2-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="39ea2-155">Это свойство наследуется от [**\_ \_ нотифистатус**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39ea2-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39ea2-156">Remarks</span></span>

<span data-ttu-id="39ea2-157">Класс **Win32 \_ привилежесстатус** является производным от [**\_ \_ екстендедстатус**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="39ea2-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39ea2-158">Требования</span><span class="sxs-lookup"><span data-stu-id="39ea2-158">Requirements</span></span>



| <span data-ttu-id="39ea2-159">Требование</span><span class="sxs-lookup"><span data-stu-id="39ea2-159">Requirement</span></span> | <span data-ttu-id="39ea2-160">Значение</span><span class="sxs-lookup"><span data-stu-id="39ea2-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39ea2-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39ea2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="39ea2-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39ea2-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="39ea2-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39ea2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="39ea2-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39ea2-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="39ea2-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39ea2-165">Namespace</span></span><br/>                | <span data-ttu-id="39ea2-166">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="39ea2-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="39ea2-167">MOF</span><span class="sxs-lookup"><span data-stu-id="39ea2-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39ea2-168"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39ea2-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ea2-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39ea2-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ea2-170">**\_\_екстендедстатус**</span><span class="sxs-lookup"><span data-stu-id="39ea2-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




