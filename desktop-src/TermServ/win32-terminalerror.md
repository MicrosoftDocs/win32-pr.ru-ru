---
title: Класс Win32_TerminalError
description: Представляет ошибку терминала.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalError службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalError, описание
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135379"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="b4d25-105">\_Класс Win32 терминалеррор</span><span class="sxs-lookup"><span data-stu-id="b4d25-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="b4d25-106">Представляет ошибку терминала.</span><span class="sxs-lookup"><span data-stu-id="b4d25-106">Represents a terminal error.</span></span>

<span data-ttu-id="b4d25-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b4d25-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4d25-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="b4d25-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b4d25-109">Members</span></span>

<span data-ttu-id="b4d25-110">Класс **Win32 \_ терминалеррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b4d25-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="b4d25-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4d25-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4d25-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b4d25-112">Properties</span></span>

<span data-ttu-id="b4d25-113">Класс **Win32 \_ терминалеррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b4d25-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4d25-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4d25-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b4d25-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-117">Любая определяемая пользователем строка, описывающая ошибку или оперативное состояние.</span><span class="sxs-lookup"><span data-stu-id="b4d25-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="b4d25-118">Это свойство наследуется от [**\_ \_ екстендедстатус**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b4d25-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b4d25-119">**Операция**</span><span class="sxs-lookup"><span data-stu-id="b4d25-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b4d25-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-122">Операция, выполняемая во время сбоя или аномалии.</span><span class="sxs-lookup"><span data-stu-id="b4d25-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="b4d25-123">Как правило, Инструментарий WMI задает для этого свойства имя API COM для метода WMI, например: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="b4d25-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="b4d25-124">Это свойство наследуется от [**\_ \_ екстендедстатус**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b4d25-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b4d25-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="b4d25-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b4d25-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-128">Параметры, участвующие в изменении состояния или ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4d25-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="b4d25-129">Например, если приложение пытается извлечь несуществующий класс, для этого свойства задается имя класса, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="b4d25-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="b4d25-130">Это свойство наследуется от [**\_ \_ екстендедстатус**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b4d25-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b4d25-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b4d25-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b4d25-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-134">Определяет поставщика, который вызывает или сообщает об ошибке или изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="b4d25-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="b4d25-135">Если поставщик не задействован, для этой строки задается значение "Управление Windows".</span><span class="sxs-lookup"><span data-stu-id="b4d25-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="b4d25-136">Это свойство наследуется от [**\_ \_ екстендедстатус**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="b4d25-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b4d25-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="b4d25-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b4d25-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-140">Содержит код ошибки или сведения для операции.</span><span class="sxs-lookup"><span data-stu-id="b4d25-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="b4d25-141">Это может быть любое значение, определенное поставщиком, но значение 0 (нуль) обычно зарезервировано для обозначения успеха.</span><span class="sxs-lookup"><span data-stu-id="b4d25-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="b4d25-142">Это свойство наследуется от [**\_ \_ нотифистатус**](/windows/desktop/WmiSdk/--notifystatus).</span><span class="sxs-lookup"><span data-stu-id="b4d25-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="b4d25-143">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="b4d25-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4d25-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b4d25-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4d25-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b4d25-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b4d25-146">Имя терминала, который произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="b4d25-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4d25-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b4d25-147">Requirements</span></span>



| <span data-ttu-id="b4d25-148">Требование</span><span class="sxs-lookup"><span data-stu-id="b4d25-148">Requirement</span></span> | <span data-ttu-id="b4d25-149">Значение</span><span class="sxs-lookup"><span data-stu-id="b4d25-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d25-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4d25-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d25-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4d25-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4d25-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4d25-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d25-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4d25-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4d25-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4d25-154">Namespace</span></span><br/>                | <span data-ttu-id="b4d25-155">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b4d25-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b4d25-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b4d25-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4d25-157"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4d25-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4d25-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b4d25-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4d25-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4d25-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4d25-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4d25-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d25-161">**\_\_екстендедстатус**</span><span class="sxs-lookup"><span data-stu-id="b4d25-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

