---
description: Используется для передачи подробных сведений о состоянии и ошибке.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Класс __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713114"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="b5ab3-103">\_\_Класс Екстендедстатус</span><span class="sxs-lookup"><span data-stu-id="b5ab3-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="b5ab3-104">Класс System **\_ \_ екстендедстатус** используется для передачи подробных сведений о состоянии и ошибках.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="b5ab3-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5ab3-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ab3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5ab3-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="b5ab3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b5ab3-108">Members</span></span>

<span data-ttu-id="b5ab3-109">Класс **\_ \_ екстендедстатус** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b5ab3-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="b5ab3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5ab3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5ab3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5ab3-111">Properties</span></span>

<span data-ttu-id="b5ab3-112">Класс **\_ \_ екстендедстатус** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5ab3-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ab3-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ab3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5ab3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ab3-116">Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="b5ab3-117">**Операция**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ab3-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ab3-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5ab3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ab3-120">Операция, выполняемая во время сбоя или аномалии.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="b5ab3-121">Как правило, инструментарий управления Windows (WMI) (WMI) задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="b5ab3-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="b5ab3-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ab3-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ab3-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5ab3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ab3-125">Параметры, участвующие в изменении состояния или ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="b5ab3-126">Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="b5ab3-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ab3-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5ab3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5ab3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ab3-130">Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="b5ab3-131">Если поставщик не задействован, для этой строки задается значение "Управление Windows".</span><span class="sxs-lookup"><span data-stu-id="b5ab3-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="b5ab3-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5ab3-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5ab3-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5ab3-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5ab3-135">Содержит код ошибки или сведения для операции.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="b5ab3-136">Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="b5ab3-137">Это свойство наследуется от [**\_ \_ нотифистатус**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="b5ab3-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5ab3-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5ab3-138">Remarks</span></span>

<span data-ttu-id="b5ab3-139">Класс **\_ \_ екстендедстатус** является производным от класса [**\_ \_ нотифистатус**](--notifystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b5ab3-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="b5ab3-140">Используйте класс **\_ \_ екстендедстатус** , чтобы сообщить более сложную информацию, чем простой код результата.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="b5ab3-141">Поставщики могут создавать собственные классы от **\_ \_ екстендедстатус** , если им требуются дополнительные свойства для описания ошибок.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="b5ab3-142">Свойство **StatusCode** , унаследованное от родительского класса [**\_ \_ нотифистатус**](--notifystatus.md) , представляет собой целое число без знака, представляющее ошибку или значение состояния.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="b5ab3-143">Когда экземпляры этого класса возвращаются из метода динамическим поставщиком, свойства **StatusCode** и **Description** задаются поставщиком, а другие свойства устанавливаются WMI.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="b5ab3-144">Примеры</span><span class="sxs-lookup"><span data-stu-id="b5ab3-144">Examples</span></span>

<span data-ttu-id="b5ab3-145">Следующий пример кода, взятый из [FND: как выполнять обработку Configuration Manager асинхронных ошибок с помощью](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) примера кода на языке сценариев VBScript в коллекции TechNet, описывает использование **\_ \_ екстендедстатус** для получения сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="b5ab3-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="b5ab3-146">Требования</span><span class="sxs-lookup"><span data-stu-id="b5ab3-146">Requirements</span></span>



| <span data-ttu-id="b5ab3-147">Требование</span><span class="sxs-lookup"><span data-stu-id="b5ab3-147">Requirement</span></span> | <span data-ttu-id="b5ab3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="b5ab3-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b5ab3-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5ab3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ab3-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ab3-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b5ab3-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5ab3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ab3-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ab3-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b5ab3-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b5ab3-153">Namespace</span></span><br/>                | <span data-ttu-id="b5ab3-154">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="b5ab3-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b5ab3-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5ab3-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ab3-156">**\_\_нотифистатус**</span><span class="sxs-lookup"><span data-stu-id="b5ab3-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="b5ab3-157">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="b5ab3-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

