---
description: '\_Класс WMI сериалпортконфигуратион для Win32 представляет параметры передачи данных в последовательном порте на основе Windows. К ним относятся конфигурации для установления соединения и проверки ошибок.'
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Класс Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990388"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="9bef9-104">\_Класс Win32 сериалпортконфигуратион</span><span class="sxs-lookup"><span data-stu-id="9bef9-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="9bef9-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ сериалпортконфигуратион для Win32** представляет параметры передачи данных в последовательном порте на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="9bef9-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="9bef9-106">К ним относятся конфигурации для установления соединения и проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="9bef9-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="9bef9-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9bef9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9bef9-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9bef9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bef9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bef9-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="9bef9-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9bef9-110">Members</span></span>

<span data-ttu-id="9bef9-111">Класс **Win32 \_ сериалпортконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bef9-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="9bef9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bef9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9bef9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bef9-113">Properties</span></span>

<span data-ttu-id="9bef9-114">Класс **Win32 \_ сериалпортконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bef9-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bef9-115">**абортреадвритеонеррор**</span><span class="sxs-lookup"><span data-stu-id="9bef9-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-118">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фабортонеррор")</span><span class="sxs-lookup"><span data-stu-id="9bef9-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-119">Если задано **значение true**, операции чтения и записи завершаются при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="9bef9-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="9bef9-120">Если **значение — true**, драйвер прерывает все операции чтения и записи с состоянием ошибки в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="9bef9-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="9bef9-121">Драйвер не будет принимать дальнейшие операции связи, пока приложение не подтвердит ошибку.</span><span class="sxs-lookup"><span data-stu-id="9bef9-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-122">**Порта**</span><span class="sxs-lookup"><span data-stu-id="9bef9-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-125">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| скорость")</span><span class="sxs-lookup"><span data-stu-id="9bef9-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-126">Скорость (в битах в секунду), с которой работает коммуникационное устройство.</span><span class="sxs-lookup"><span data-stu-id="9bef9-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="9bef9-127">Пример: 9600</span><span class="sxs-lookup"><span data-stu-id="9bef9-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-128">**бинаримодинаблед**</span><span class="sxs-lookup"><span data-stu-id="9bef9-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-131">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фбинари")</span><span class="sxs-lookup"><span data-stu-id="9bef9-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-132">Если задано **значение true**, передача данных в двоичном режиме включается для последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="9bef9-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="9bef9-133">Компьютерные системы, работающие под Windows, разрешают только двоичные передачи через последовательные порты, поэтому это значение всегда равно **true**.</span><span class="sxs-lookup"><span data-stu-id="9bef9-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-134">**битспербите**</span><span class="sxs-lookup"><span data-stu-id="9bef9-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| битесизе")</span><span class="sxs-lookup"><span data-stu-id="9bef9-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-138">Количество бит, переданных и полученных для каждого байта данных для последовательного порта Windows.</span><span class="sxs-lookup"><span data-stu-id="9bef9-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="9bef9-139">Это число может отличаться в зависимости от разрядов контроля и исправления ошибок, например битов четности.</span><span class="sxs-lookup"><span data-stu-id="9bef9-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="9bef9-140">Пример: 8</span><span class="sxs-lookup"><span data-stu-id="9bef9-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-141">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9bef9-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-144">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="9bef9-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-145">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="9bef9-145">Short textual description of the current object.</span></span>

<span data-ttu-id="9bef9-146">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9bef9-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-147">**континуексмитонксофф**</span><span class="sxs-lookup"><span data-stu-id="9bef9-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-150">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фтксконтинуеонксофф")</span><span class="sxs-lookup"><span data-stu-id="9bef9-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-151">Если **значение равно true**, передача данных продолжается, когда входной буфер поступает в пределах **ксоффксмитсрешолд** байт и драйвер передал значение **ксоффчарарктер** для прекращения получения байтов.</span><span class="sxs-lookup"><span data-stu-id="9bef9-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="9bef9-152">Если **значение равно false**, передача не продолжается до тех пор, пока входной буфер не будет **ксонксмитсрешолд** байт, а драйвер передал значение **ксончарактер** , чтобы возобновить прием.</span><span class="sxs-lookup"><span data-stu-id="9bef9-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-153">**ктсаутфловконтрол**</span><span class="sxs-lookup"><span data-stu-id="9bef9-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-154">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-156">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фаутксктсфлов")</span><span class="sxs-lookup"><span data-stu-id="9bef9-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-157">Если задано **значение true**, то перед передачей данных проверяется сигнал CTS.</span><span class="sxs-lookup"><span data-stu-id="9bef9-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="9bef9-158">CTS сигнализирует, что оба устройства в последовательном подключении готовы к передаче данных.</span><span class="sxs-lookup"><span data-stu-id="9bef9-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="9bef9-159">Передача данных приостанавливается до тех пор, пока не будет задан сигнал CTS.</span><span class="sxs-lookup"><span data-stu-id="9bef9-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-160">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9bef9-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-163">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="9bef9-163">Textual description of the current object.</span></span>

<span data-ttu-id="9bef9-164">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9bef9-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-165">**дискарднуллбитес**</span><span class="sxs-lookup"><span data-stu-id="9bef9-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-166">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-168">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| значение fNull")</span><span class="sxs-lookup"><span data-stu-id="9bef9-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-169">Если **значение равно true**, **пустые** байты (символы) отбрасываются при получении.</span><span class="sxs-lookup"><span data-stu-id="9bef9-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-170">**дсраутфловконтрол**</span><span class="sxs-lookup"><span data-stu-id="9bef9-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-171">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-173">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фаутксдсрфлов")</span><span class="sxs-lookup"><span data-stu-id="9bef9-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-174">Если **значение — true**, управление потоком данных включено, если имеется условие готовности набора данных (DSR).</span><span class="sxs-lookup"><span data-stu-id="9bef9-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="9bef9-175">DSR сигнализирует, что подключение было установлено устройствами через последовательное подключение.</span><span class="sxs-lookup"><span data-stu-id="9bef9-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="9bef9-176">Передача данных DSR приостанавливается до тех пор, пока не будет указан сигнал DSR.</span><span class="sxs-lookup"><span data-stu-id="9bef9-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-177">**Чувствительность DSR**</span><span class="sxs-lookup"><span data-stu-id="9bef9-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-178">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-180">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фдсрсенситивити")</span><span class="sxs-lookup"><span data-stu-id="9bef9-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-181">Если **значение — true**, драйвер связи чувствителен к состоянию сигнала DSR.</span><span class="sxs-lookup"><span data-stu-id="9bef9-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="9bef9-182">Драйвер игнорирует все полученные байты, если входная линия коммутатора DSR не является высокой.</span><span class="sxs-lookup"><span data-stu-id="9bef9-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-183">**дтрфловконтролтипе**</span><span class="sxs-lookup"><span data-stu-id="9bef9-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-186">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фдтрконтрол")</span><span class="sxs-lookup"><span data-stu-id="9bef9-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-187">Использование управления потоком терминала данных (DTR) после установления соединения.</span><span class="sxs-lookup"><span data-stu-id="9bef9-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="9bef9-188">**Enable** ("включить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="9bef9-189">**Отключить** ("отключить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="9bef9-190">**Подтверждение** ("подтверждение")</span><span class="sxs-lookup"><span data-stu-id="9bef9-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9bef9-191">**Символ конца файла**</span><span class="sxs-lookup"><span data-stu-id="9bef9-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-192">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-194">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| еофчар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-195">Значение символа, используемого для обозначения конца данных.</span><span class="sxs-lookup"><span data-stu-id="9bef9-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="9bef9-196">Пример: ^ Z</span><span class="sxs-lookup"><span data-stu-id="9bef9-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-197">**еррорреплацечарактер**</span><span class="sxs-lookup"><span data-stu-id="9bef9-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-200">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| еррорчар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-201">Значение символа, используемого для замены полученных байтов с ошибкой четности.</span><span class="sxs-lookup"><span data-stu-id="9bef9-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="9bef9-202">Пример: ^ C</span><span class="sxs-lookup"><span data-stu-id="9bef9-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-203">**еррорреплацементенаблед**</span><span class="sxs-lookup"><span data-stu-id="9bef9-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-204">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-206">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| феррорчар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-207">Если **значение равно true**, байты, полученные с ошибками четности, заменяются значением **еррорреплацечарактер** .</span><span class="sxs-lookup"><span data-stu-id="9bef9-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="9bef9-208">Символы с ошибками четности заменяются только в том случае, если это свойство имеет **значение true** , а проверка четности включена.</span><span class="sxs-lookup"><span data-stu-id="9bef9-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-209">**евентчарактер**</span><span class="sxs-lookup"><span data-stu-id="9bef9-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-210">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-212">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| евтчар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-213">Значение управляющего символа, который используется для сигнализации события, например конца файла.</span><span class="sxs-lookup"><span data-stu-id="9bef9-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="9bef9-214">Пример: ^ e</span><span class="sxs-lookup"><span data-stu-id="9bef9-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-215">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="9bef9-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-218">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| File functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="9bef9-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-219">**Значение true** показывает, что последовательный порт занят.</span><span class="sxs-lookup"><span data-stu-id="9bef9-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-220">**Name**</span><span class="sxs-lookup"><span data-stu-id="9bef9-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-223">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| оборудование \\ \\ девицемап \\ \\ сериалкомм")</span><span class="sxs-lookup"><span data-stu-id="9bef9-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-224">Имя последовательного порта Windows.</span><span class="sxs-lookup"><span data-stu-id="9bef9-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="9bef9-225">Пример: "COM1"</span><span class="sxs-lookup"><span data-stu-id="9bef9-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-226">**Parity**</span><span class="sxs-lookup"><span data-stu-id="9bef9-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-229">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| четность")</span><span class="sxs-lookup"><span data-stu-id="9bef9-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-230">Метод проверки четности для использования.</span><span class="sxs-lookup"><span data-stu-id="9bef9-230">Method of parity checking to be used.</span></span> <span data-ttu-id="9bef9-231">В качестве метода проверки ошибок используется четность, при котором каждая единица данных включает дополнительный бит четности.</span><span class="sxs-lookup"><span data-stu-id="9bef9-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="9bef9-232">Затем получатель может проверить допустимость данных, подчисляя заданные биты.</span><span class="sxs-lookup"><span data-stu-id="9bef9-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="9bef9-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** ("нет")</span><span class="sxs-lookup"><span data-stu-id="9bef9-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-234">Проверка четности не используется.</span><span class="sxs-lookup"><span data-stu-id="9bef9-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="9bef9-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Нечетная** ("нечетная")</span><span class="sxs-lookup"><span data-stu-id="9bef9-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-236">Устанавливает бит четности так, чтобы число установленных битов всегда было нечетным.</span><span class="sxs-lookup"><span data-stu-id="9bef9-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="9bef9-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Даже** ("даже")</span><span class="sxs-lookup"><span data-stu-id="9bef9-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-238">Устанавливает бит четности так, чтобы число установленных битов всегда было четным.</span><span class="sxs-lookup"><span data-stu-id="9bef9-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="9bef9-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Пометить** ("пометить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-240">Оставляет бит четности равным 1.</span><span class="sxs-lookup"><span data-stu-id="9bef9-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="9bef9-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Пробел** ("пробел")</span><span class="sxs-lookup"><span data-stu-id="9bef9-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-242">Оставляет бит четности со значением 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="9bef9-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9bef9-243">**паритичеккенаблед**</span><span class="sxs-lookup"><span data-stu-id="9bef9-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-244">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bef9-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-246">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фпарити")</span><span class="sxs-lookup"><span data-stu-id="9bef9-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-247">Если **значение равно true**, проверка четности включена.</span><span class="sxs-lookup"><span data-stu-id="9bef9-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-248">**ртсфловконтролтипе**</span><span class="sxs-lookup"><span data-stu-id="9bef9-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-251">Управление потоком запроса на отправку (RTS).</span><span class="sxs-lookup"><span data-stu-id="9bef9-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="9bef9-252">RTS используется для сигнализации того, что данные доступны для передачи.</span><span class="sxs-lookup"><span data-stu-id="9bef9-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="9bef9-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("включить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-254">Для сеанса обмена данными остается RTS.</span><span class="sxs-lookup"><span data-stu-id="9bef9-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="9bef9-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** ("отключить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-256">RTS игнорируется после получения первого сигнала RTS.</span><span class="sxs-lookup"><span data-stu-id="9bef9-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="9bef9-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Подтверждение** ("подтверждение")</span><span class="sxs-lookup"><span data-stu-id="9bef9-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-258">RTS отключается, если размер буфера передачи превышает три квартала, а RTS включен, если буфер меньше единицы заполнения.</span><span class="sxs-lookup"><span data-stu-id="9bef9-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="9bef9-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Переключатель** ("переключить")</span><span class="sxs-lookup"><span data-stu-id="9bef9-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-260">RTS включается при наличии данных, буферизованных для передачи.</span><span class="sxs-lookup"><span data-stu-id="9bef9-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9bef9-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="9bef9-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-264">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="9bef9-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-265">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="9bef9-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="9bef9-266">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9bef9-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-267">**стопбитс**</span><span class="sxs-lookup"><span data-stu-id="9bef9-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-268">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bef9-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-270">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| стопбитс")</span><span class="sxs-lookup"><span data-stu-id="9bef9-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-271">Число используемых битов.</span><span class="sxs-lookup"><span data-stu-id="9bef9-271">Number of stop bits to be used.</span></span> <span data-ttu-id="9bef9-272">Останавливаются биты, разделяющие каждую единицу данных на асинхронном последовательном подключении.</span><span class="sxs-lookup"><span data-stu-id="9bef9-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="9bef9-273">Они также отправляются постоянно, когда нет доступных данных для передачи.</span><span class="sxs-lookup"><span data-stu-id="9bef9-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9bef9-274">**1** ("1")</span><span class="sxs-lookup"><span data-stu-id="9bef9-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="9bef9-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="9bef9-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="9bef9-276">**2** ("2")</span><span class="sxs-lookup"><span data-stu-id="9bef9-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9bef9-277">**ксоффчарактер**</span><span class="sxs-lookup"><span data-stu-id="9bef9-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-278">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-280">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксоффчар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-281">Значение символа XOFF для передачи и приема.</span><span class="sxs-lookup"><span data-stu-id="9bef9-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="9bef9-282">XOFF — это программный элемент управления для отключения передачи данных (в то время как RTS и CTS — аппаратные элементы управления).</span><span class="sxs-lookup"><span data-stu-id="9bef9-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="9bef9-283">XON возобновляет передачу.</span><span class="sxs-lookup"><span data-stu-id="9bef9-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-284">**ксоффксмитсрешолд**</span><span class="sxs-lookup"><span data-stu-id="9bef9-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-285">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-287">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксоффлим")</span><span class="sxs-lookup"><span data-stu-id="9bef9-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-288">Максимальное число байтов, разрешенное во входном буфере до отправки символа XOFF.</span><span class="sxs-lookup"><span data-stu-id="9bef9-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-289">**ксончарактер**</span><span class="sxs-lookup"><span data-stu-id="9bef9-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-290">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-292">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксончар")</span><span class="sxs-lookup"><span data-stu-id="9bef9-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-293">Значение символа XON как для передачи, так и для приема.</span><span class="sxs-lookup"><span data-stu-id="9bef9-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="9bef9-294">XON — это программный элемент управления для возобновления передачи данных (тогда как RTS и CTS — аппаратные элементы управления).</span><span class="sxs-lookup"><span data-stu-id="9bef9-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="9bef9-295">XOFF останавливает передачу.</span><span class="sxs-lookup"><span data-stu-id="9bef9-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-296">**ксонксмитсрешолд**</span><span class="sxs-lookup"><span data-stu-id="9bef9-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-297">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-299">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ксонлим")</span><span class="sxs-lookup"><span data-stu-id="9bef9-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-300">Минимальное число байтов, разрешенное во входном буфере до отправки символа XON.</span><span class="sxs-lookup"><span data-stu-id="9bef9-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="9bef9-301">Это свойство работает совместно с **ксоффксмитсрешолд** для регулирования скорости передачи данных.</span><span class="sxs-lookup"><span data-stu-id="9bef9-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="9bef9-302">**ксонксоффинфловконтрол**</span><span class="sxs-lookup"><span data-stu-id="9bef9-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-303">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-305">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Финкс")</span><span class="sxs-lookup"><span data-stu-id="9bef9-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-306">Если задано **значение true**, во время приема используется управление потоком XON/XOFF.</span><span class="sxs-lookup"><span data-stu-id="9bef9-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="9bef9-307">Если задано значение **true**, значение **ксоффчарактер** отправляется, когда входной буфер поступает в пределах **Ксоффксмитсрешолд** байт, а значение **ксончарактер** отправляется, когда входной буфер попадает в пределы **ксонксмитсрешолд** байт.</span><span class="sxs-lookup"><span data-stu-id="9bef9-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="9bef9-308"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="9bef9-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-309">FALSE</span><span class="sxs-lookup"><span data-stu-id="9bef9-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="9bef9-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9bef9-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9bef9-311">true</span><span class="sxs-lookup"><span data-stu-id="9bef9-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9bef9-312">**ксонксоффаутфловконтрол**</span><span class="sxs-lookup"><span data-stu-id="9bef9-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bef9-313">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9bef9-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bef9-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bef9-315">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фауткс")</span><span class="sxs-lookup"><span data-stu-id="9bef9-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="9bef9-316">**Ксонксоффаутфловконтрол** указывает, используется ли управление потоком XON или XOFF во время передачи.</span><span class="sxs-lookup"><span data-stu-id="9bef9-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="9bef9-317">Если значение — **true**, передача прекращается при получении значения **ксоффчарактер** и начинается снова при получении значения **ксончарактер** .</span><span class="sxs-lookup"><span data-stu-id="9bef9-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bef9-318">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bef9-318">Remarks</span></span>

<span data-ttu-id="9bef9-319">Класс **Win32 \_ сериалпортконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="9bef9-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bef9-320">Требования</span><span class="sxs-lookup"><span data-stu-id="9bef9-320">Requirements</span></span>



| <span data-ttu-id="9bef9-321">Требование</span><span class="sxs-lookup"><span data-stu-id="9bef9-321">Requirement</span></span> | <span data-ttu-id="9bef9-322">Значение</span><span class="sxs-lookup"><span data-stu-id="9bef9-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bef9-323">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bef9-323">Minimum supported client</span></span><br/> | <span data-ttu-id="9bef9-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bef9-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9bef9-325">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bef9-325">Minimum supported server</span></span><br/> | <span data-ttu-id="9bef9-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bef9-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9bef9-327">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bef9-327">Namespace</span></span><br/>                | <span data-ttu-id="9bef9-328">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9bef9-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9bef9-329">MOF</span><span class="sxs-lookup"><span data-stu-id="9bef9-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bef9-330"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bef9-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bef9-331">DLL</span><span class="sxs-lookup"><span data-stu-id="9bef9-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bef9-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bef9-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bef9-333">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bef9-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bef9-334">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="9bef9-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="9bef9-335">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="9bef9-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
