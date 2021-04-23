---
description: Поставщик классов WDM определяет класс Вмибинаримофресаурце в \\ корневом \\ пространстве имен WMI для поддержки задачи отслеживания состояния данных в репозитории WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Класс Вмибинаримофресаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898098"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="efa2e-103">Класс Вмибинаримофресаурце</span><span class="sxs-lookup"><span data-stu-id="efa2e-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="efa2e-104">Поставщик классов WDM определяет класс **вмибинаримофресаурце** в \\ корневом \\ пространстве имен WMI для поддержки задачи отслеживания состояния данных в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="efa2e-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efa2e-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="efa2e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="efa2e-106">Members</span></span>

<span data-ttu-id="efa2e-107">Класс **вмибинаримофресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="efa2e-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="efa2e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="efa2e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efa2e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="efa2e-109">Properties</span></span>

<span data-ttu-id="efa2e-110">Класс **вмибинаримофресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="efa2e-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efa2e-111">**хигхдатетиме**</span><span class="sxs-lookup"><span data-stu-id="efa2e-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa2e-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa2e-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efa2e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="efa2e-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="efa2e-115">Старшая половина метки даты и времени.</span><span class="sxs-lookup"><span data-stu-id="efa2e-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="efa2e-116">**ловдатетиме**</span><span class="sxs-lookup"><span data-stu-id="efa2e-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa2e-117">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa2e-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efa2e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="efa2e-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="efa2e-120">Минимальная половина метки даты и времени.</span><span class="sxs-lookup"><span data-stu-id="efa2e-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="efa2e-121">**мофпроцессед**</span><span class="sxs-lookup"><span data-stu-id="efa2e-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa2e-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="efa2e-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="efa2e-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="efa2e-124">Флаг, указывающий, была ли MOF-файл обработана полностью.</span><span class="sxs-lookup"><span data-stu-id="efa2e-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="efa2e-125">**Name**</span><span class="sxs-lookup"><span data-stu-id="efa2e-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa2e-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="efa2e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="efa2e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efa2e-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="efa2e-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="efa2e-129">Имя драйвера с поддержкой WDM, который содержит двоичный MOF-файл, успешно скомпилированный в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="efa2e-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efa2e-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efa2e-130">Remarks</span></span>

<span data-ttu-id="efa2e-131">Поставщик классов WDM создает экземпляр **вмибинаримофресаурце** для каждого драйвера WDM, который предоставляет двоичный MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="efa2e-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="efa2e-132">Всякий раз, когда инструментарий WMI Инициализирует поставщик, поставщик сравнивает метку времени с меткой времени файла изображения драйвера.</span><span class="sxs-lookup"><span data-stu-id="efa2e-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="efa2e-133">Если метки времени отличаются, WMI повторно компилирует MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="efa2e-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="efa2e-134">Требования</span><span class="sxs-lookup"><span data-stu-id="efa2e-134">Requirements</span></span>



| <span data-ttu-id="efa2e-135">Требование</span><span class="sxs-lookup"><span data-stu-id="efa2e-135">Requirement</span></span> | <span data-ttu-id="efa2e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="efa2e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="efa2e-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efa2e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="efa2e-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="efa2e-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="efa2e-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efa2e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="efa2e-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efa2e-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="efa2e-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="efa2e-141">Namespace</span></span><br/>                | <span data-ttu-id="efa2e-142">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="efa2e-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="efa2e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="efa2e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efa2e-144"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efa2e-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efa2e-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efa2e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa2e-146">Поставщик WDM</span><span class="sxs-lookup"><span data-stu-id="efa2e-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

