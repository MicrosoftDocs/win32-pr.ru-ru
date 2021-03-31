---
description: '\_Структура данных об уведомлении принтера \_ \_ определяет поле со сведениями о задании или принтере и предоставляет текущие данные для этого поля.'
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Структура PRINTER_NOTIFY_INFO_DATA (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264923"
---
# <a name="printer_notify_info_data-structure"></a><span data-ttu-id="91ada-103">\_ \_ Структура данных об УВЕДОМЛЕНии принтера \_</span><span class="sxs-lookup"><span data-stu-id="91ada-103">PRINTER\_NOTIFY\_INFO\_DATA structure</span></span>

<span data-ttu-id="91ada-104">Структура **\_ \_ \_ данных об уведомлении принтера** определяет поле со сведениями о задании или принтере и предоставляет текущие данные для этого поля.</span><span class="sxs-lookup"><span data-stu-id="91ada-104">The **PRINTER\_NOTIFY\_INFO\_DATA** structure identifies a job or printer information field and provides the current data for that field.</span></span>

<span data-ttu-id="91ada-105">Функция [**финднекстпринтерчанженотификатион**](findnextprinterchangenotification.md) возвращает структуру [**уведомления принтера \_ \_**](printer-notify-info.md) , которая содержит массив **информационных структур \_ \_ \_ данных принтера** .</span><span class="sxs-lookup"><span data-stu-id="91ada-105">The [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function returns a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of **PRINTER\_NOTIFY\_INFO\_DATA** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ada-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91ada-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a><span data-ttu-id="91ada-107">Члены</span><span class="sxs-lookup"><span data-stu-id="91ada-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="91ada-108">**Тип**</span><span class="sxs-lookup"><span data-stu-id="91ada-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-109">Указывает тип предоставленных сведений.</span><span class="sxs-lookup"><span data-stu-id="91ada-109">Indicates the type of information provided.</span></span> <span data-ttu-id="91ada-110">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="91ada-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="91ada-111">Значение</span><span class="sxs-lookup"><span data-stu-id="91ada-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="91ada-112">Значение</span><span class="sxs-lookup"><span data-stu-id="91ada-112">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="91ada-113"><dt>**Задание \_ УВЕДОМЛЕНИЕ \_ типа**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="91ada-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="91ada-114">Указывает, что член **поля** указывает \_ \_ \_ \* константу поля уведомления задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-114">Indicates that the **Field** member specifies a JOB\_NOTIFY\_FIELD\_\* constant.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="91ada-115"><dt>**Принтер \_ УВЕДОМЛЕНИЕ \_ типа**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="91ada-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="91ada-116">Указывает, что член **поля** указывает \_ \_ \_ \* константу поля для уведомления принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-116">Indicates that the **Field** member specifies a PRINTER\_NOTIFY\_FIELD\_\* constant.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="91ada-117">**Поле**</span><span class="sxs-lookup"><span data-stu-id="91ada-117">**Field**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-118">Указывает измененное поле.</span><span class="sxs-lookup"><span data-stu-id="91ada-118">Indicates the field that changed.</span></span> <span data-ttu-id="91ada-119">Список возможных значений см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="91ada-119">For a list of possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="91ada-120">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="91ada-120">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="91ada-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="91ada-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="91ada-122">**Id**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-123">Указывает идентификатор задания, если член **типа** указывает \_ тип уведомления задания \_ .</span><span class="sxs-lookup"><span data-stu-id="91ada-123">Indicates the job identifier if the **Type** member specifies JOB\_NOTIFY\_TYPE.</span></span> <span data-ttu-id="91ada-124">Если член **типа** указывает \_ тип уведомления принтера \_ , этот член не определен.</span><span class="sxs-lookup"><span data-stu-id="91ada-124">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="91ada-125">**нотифидата**</span><span class="sxs-lookup"><span data-stu-id="91ada-125">**NotifyData**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-126">Объединение сведений о данных на основе **типа** и членов **поля** .</span><span class="sxs-lookup"><span data-stu-id="91ada-126">A union of data information based on the **Type** and **Field** members.</span></span> <span data-ttu-id="91ada-127">Описание типа данных, связанных с каждым полем, см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="91ada-127">For a description of the type of data associated with each field, see the Remarks section.</span></span>

<dl> <dt>

<span data-ttu-id="91ada-128">**Адвдата \[ 2\]**</span><span class="sxs-lookup"><span data-stu-id="91ada-128">**adwData\[2\]**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-129">Массив из двух значений **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="91ada-129">An array of two **DWORD** values.</span></span> <span data-ttu-id="91ada-130">Для информационных полей, использующих только один **DWORD**, данные находятся в **адвдата** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="91ada-130">For information fields that use only a single **DWORD**, the data is in **adwData** \[0\].</span></span>

</dd> <dt>

<span data-ttu-id="91ada-131">**Data**</span><span class="sxs-lookup"><span data-stu-id="91ada-131">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91ada-132">**кббуф**</span><span class="sxs-lookup"><span data-stu-id="91ada-132">**cbBuf**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-133">Указывает размер (в байтах) буфера, на который указывает **пбуф**.</span><span class="sxs-lookup"><span data-stu-id="91ada-133">Indicates the size, in bytes, of the buffer pointed to by **pBuf**.</span></span>

</dd> <dt>

<span data-ttu-id="91ada-134">**пбуф**</span><span class="sxs-lookup"><span data-stu-id="91ada-134">**pBuf**</span></span>
</dt> <dd>

<span data-ttu-id="91ada-135">Указатель на буфер, содержащий текущие данные поля.</span><span class="sxs-lookup"><span data-stu-id="91ada-135">Pointer to a buffer that contains the field's current data.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91ada-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91ada-136">Remarks</span></span>

<span data-ttu-id="91ada-137">Если член **типа** указывает \_ тип уведомления принтера \_ , элемент **field** может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="91ada-137">If the **Type** member specifies PRINTER\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="91ada-138">Поле</span><span class="sxs-lookup"><span data-stu-id="91ada-138">Field</span></span></th>
<th><span data-ttu-id="91ada-139">Тип данных</span><span class="sxs-lookup"><span data-stu-id="91ada-139">Type of data</span></span></th>
<th><span data-ttu-id="91ada-140">Значение</span><span class="sxs-lookup"><span data-stu-id="91ada-140">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91ada-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-141">PRINTER_NOTIFY_FIELD_SERVER_NAME</span></span></td>
<td><span data-ttu-id="91ada-142">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-142">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-143">0x00</span><span class="sxs-lookup"><span data-stu-id="91ada-143">0x00</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-144">PRINTER_NOTIFY_FIELD_PRINTER_NAME</span></span></td>
<td><span data-ttu-id="91ada-145"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая содержит имя принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-145"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer.</span></span></td>
<td><span data-ttu-id="91ada-146">0x01</span><span class="sxs-lookup"><span data-stu-id="91ada-146">0x01</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-147">PRINTER_NOTIFY_FIELD_SHARE_NAME</span></span></td>
<td><span data-ttu-id="91ada-148"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая определяет общую точку печати для принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-148"><strong>pBuf</strong> is a pointer to a null-terminated string that identifies the share point for the printer.</span></span></td>
<td><span data-ttu-id="91ada-149">0x02</span><span class="sxs-lookup"><span data-stu-id="91ada-149">0x02</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-150">PRINTER_NOTIFY_FIELD_PORT_NAME</span></span></td>
<td><span data-ttu-id="91ada-151"><strong>пбуф</strong> — это указатель на строку с завершающим нулем, содержащую имя порта, в который будут печататься задания печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-151"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the port that the print jobs will be printed to.</span></span> <span data-ttu-id="91ada-152">Если &quot; выбрана группировка принтеров &quot; , это список портов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="91ada-152">If &quot;Printer Pooling&quot; is selected, this is a comma separated list of ports.</span></span></td>
<td><span data-ttu-id="91ada-153">0x03</span><span class="sxs-lookup"><span data-stu-id="91ada-153">0x03</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-154">PRINTER_NOTIFY_FIELD_DRIVER_NAME</span></span></td>
<td><span data-ttu-id="91ada-155"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая содержит имя драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-155"><strong>pBuf</strong> is a pointer to a null-terminated string containing the name of the printer's driver.</span></span></td>
<td><span data-ttu-id="91ada-156">0x04</span><span class="sxs-lookup"><span data-stu-id="91ada-156">0x04</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-157">PRINTER_NOTIFY_FIELD_COMMENT</span><span class="sxs-lookup"><span data-stu-id="91ada-157">PRINTER_NOTIFY_FIELD_COMMENT</span></span></td>
<td><span data-ttu-id="91ada-158"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, содержащую новую строку комментария, которая обычно является кратким описанием принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-158"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new comment string, which is typically a brief description of the printer.</span></span></td>
<td><span data-ttu-id="91ada-159">0x05</span><span class="sxs-lookup"><span data-stu-id="91ada-159">0x05</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-160">PRINTER_NOTIFY_FIELD_LOCATION</span><span class="sxs-lookup"><span data-stu-id="91ada-160">PRINTER_NOTIFY_FIELD_LOCATION</span></span></td>
<td><span data-ttu-id="91ada-161"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая содержит новое физическое расположение принтера (например, &quot; Блдг.</span><span class="sxs-lookup"><span data-stu-id="91ada-161"><strong>pBuf</strong> is a pointer to a null-terminated string containing the new physical location of the printer (for example, &quot;Bldg.</span></span> <span data-ttu-id="91ada-162">38, комната 1164 &quot; ).</span><span class="sxs-lookup"><span data-stu-id="91ada-162">38, Room 1164&quot;).</span></span></td>
<td><span data-ttu-id="91ada-163">0x06</span><span class="sxs-lookup"><span data-stu-id="91ada-163">0x06</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-164">PRINTER_NOTIFY_FIELD_DEVMODE</span><span class="sxs-lookup"><span data-stu-id="91ada-164">PRINTER_NOTIFY_FIELD_DEVMODE</span></span></td>
<td><span data-ttu-id="91ada-165"><strong>пбуф</strong> — это указатель на структуру <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> , которая определяет данные принтера по умолчанию, такие как ориентация бумаги и разрешение.</span><span class="sxs-lookup"><span data-stu-id="91ada-165"><strong>pBuf</strong> is a pointer to a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> structure that defines default printer data such as the paper orientation and the resolution.</span></span></td>
<td><span data-ttu-id="91ada-166">0x07</span><span class="sxs-lookup"><span data-stu-id="91ada-166">0x07</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-167">PRINTER_NOTIFY_FIELD_SEPFILE</span><span class="sxs-lookup"><span data-stu-id="91ada-167">PRINTER_NOTIFY_FIELD_SEPFILE</span></span></td>
<td><span data-ttu-id="91ada-168"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая указывает имя файла, используемого для создания страницы-разделителя.</span><span class="sxs-lookup"><span data-stu-id="91ada-168"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="91ada-169">Эта страница используется для разделения заданий печати, отправленных на принтер.</span><span class="sxs-lookup"><span data-stu-id="91ada-169">This page is used to separate print jobs sent to the printer.</span></span></td>
<td><span data-ttu-id="91ada-170">0x08</span><span class="sxs-lookup"><span data-stu-id="91ada-170">0x08</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="91ada-171">PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</span></span></td>
<td><span data-ttu-id="91ada-172"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати, используемого принтером.</span><span class="sxs-lookup"><span data-stu-id="91ada-172"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span></td>
<td><span data-ttu-id="91ada-173">0x09</span><span class="sxs-lookup"><span data-stu-id="91ada-173">0x09</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91ada-174">PRINTER_NOTIFY_FIELD_PARAMETERS</span></span></td>
<td><span data-ttu-id="91ada-175"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая указывает параметры по умолчанию для обработчика печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-175"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the default print-processor parameters.</span></span></td>
<td><span data-ttu-id="91ada-176">0x0A</span><span class="sxs-lookup"><span data-stu-id="91ada-176">0x0A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-177">PRINTER_NOTIFY_FIELD_DATATYPE</span><span class="sxs-lookup"><span data-stu-id="91ada-177">PRINTER_NOTIFY_FIELD_DATATYPE</span></span></td>
<td><span data-ttu-id="91ada-178"><strong>пбуф</strong> — это указатель на строку, завершающуюся нулем, которая указывает тип данных, используемый для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-178"><strong>pBuf</strong> is a pointer to a null-terminated string that specifies the data type used to record the print job.</span></span></td>
<td><span data-ttu-id="91ada-179">0x0B</span><span class="sxs-lookup"><span data-stu-id="91ada-179">0x0B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span><span class="sxs-lookup"><span data-stu-id="91ada-180">PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</span></span></td>
<td><span data-ttu-id="91ada-181"><strong>пбуф</strong> — это указатель на структуру <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> для принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-181"><strong>pBuf</strong> is a pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> structure for the printer.</span></span> <span data-ttu-id="91ada-182">Указатель может иметь <strong>значение NULL</strong> , если дескриптор безопасности отсутствует.</span><span class="sxs-lookup"><span data-stu-id="91ada-182">The pointer may be <strong>NULL</strong> if there is no security descriptor.</span></span></td>
<td><span data-ttu-id="91ada-183">0x0C</span><span class="sxs-lookup"><span data-stu-id="91ada-183">0x0C</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="91ada-184">PRINTER_NOTIFY_FIELD_ATTRIBUTES</span></span></td>
<td><span data-ttu-id="91ada-185"><strong>адвдата</strong> [0] задает атрибуты принтера, которые могут принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="91ada-185"><strong>adwData</strong> [0] specifies the printer attributes, which can be one of the following values:</span></span><dl> <span data-ttu-id="91ada-186">PRINTER_ATTRIBUTE_QUEUED</span><span class="sxs-lookup"><span data-stu-id="91ada-186">PRINTER_ATTRIBUTE_QUEUED</span></span><br />
<span data-ttu-id="91ada-187">PRINTER_ATTRIBUTE_DIRECT</span><span class="sxs-lookup"><span data-stu-id="91ada-187">PRINTER_ATTRIBUTE_DIRECT</span></span><br />
<span data-ttu-id="91ada-188">PRINTER_ATTRIBUTE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="91ada-188">PRINTER_ATTRIBUTE_DEFAULT</span></span><br />
<span data-ttu-id="91ada-189">PRINTER_ATTRIBUTE_SHARED</span><span class="sxs-lookup"><span data-stu-id="91ada-189">PRINTER_ATTRIBUTE_SHARED</span></span><br />
</dl></td>
<td><span data-ttu-id="91ada-190">0x0D</span><span class="sxs-lookup"><span data-stu-id="91ada-190">0x0D</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-191">PRINTER_NOTIFY_FIELD_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="91ada-191">PRINTER_NOTIFY_FIELD_PRIORITY</span></span></td>
<td><span data-ttu-id="91ada-192"><strong>адвдата</strong> [0] указывает значение приоритета, используемое диспетчером очереди для маршрутизации заданий печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-192"><strong>adwData</strong> [0] specifies a priority value that the spooler uses to route print jobs.</span></span></td>
<td><span data-ttu-id="91ada-193">0x0E</span><span class="sxs-lookup"><span data-stu-id="91ada-193">0x0E</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="91ada-194">PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</span></span></td>
<td><span data-ttu-id="91ada-195"><strong>адвдата</strong> [0] указывает значение приоритета по умолчанию, назначенное каждому заданию печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-195"><strong>adwData</strong> [0] specifies the default priority value assigned to each print job.</span></span></td>
<td><span data-ttu-id="91ada-196">0x0F</span><span class="sxs-lookup"><span data-stu-id="91ada-196">0x0F</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-197">PRINTER_NOTIFY_FIELD_START_TIME</span><span class="sxs-lookup"><span data-stu-id="91ada-197">PRINTER_NOTIFY_FIELD_START_TIME</span></span></td>
<td><span data-ttu-id="91ada-198"><strong>адвдата</strong> [0] указывает самое раннее время, когда принтер будет печатать задание.</span><span class="sxs-lookup"><span data-stu-id="91ada-198"><strong>adwData</strong> [0] specifies the earliest time at which the printer will print a job.</span></span> <span data-ttu-id="91ada-199">(Это значение указывается в минутах, истекшем с 12:00 утра)</span><span class="sxs-lookup"><span data-stu-id="91ada-199">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="91ada-200">0x10</span><span class="sxs-lookup"><span data-stu-id="91ada-200">0x10</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span><span class="sxs-lookup"><span data-stu-id="91ada-201">PRINTER_NOTIFY_FIELD_UNTIL_TIME</span></span></td>
<td><span data-ttu-id="91ada-202"><strong>адвдата</strong> [0] указывает последнее время, когда принтер будет печатать задание.</span><span class="sxs-lookup"><span data-stu-id="91ada-202"><strong>adwData</strong> [0] specifies the latest time at which the printer will print a job.</span></span> <span data-ttu-id="91ada-203">(Это значение указывается в минутах, истекшем с 12:00 утра)</span><span class="sxs-lookup"><span data-stu-id="91ada-203">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span></td>
<td><span data-ttu-id="91ada-204">0x11</span><span class="sxs-lookup"><span data-stu-id="91ada-204">0x11</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-205">PRINTER_NOTIFY_FIELD_STATUS</span><span class="sxs-lookup"><span data-stu-id="91ada-205">PRINTER_NOTIFY_FIELD_STATUS</span></span></td>
<td><span data-ttu-id="91ada-206"><strong>адвдата</strong> [0] указывает состояние принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-206"><strong>adwData</strong> [0] specifies the printer status.</span></span> <span data-ttu-id="91ada-207">Список возможных значений см. в разделе Структура <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="91ada-207">For a list of possible values, see the <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> structure.</span></span></td>
<td><span data-ttu-id="91ada-208">0x12</span><span class="sxs-lookup"><span data-stu-id="91ada-208">0x12</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span><span class="sxs-lookup"><span data-stu-id="91ada-209">PRINTER_NOTIFY_FIELD_STATUS_STRING</span></span></td>
<td><span data-ttu-id="91ada-210">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-210">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-211">0x13</span><span class="sxs-lookup"><span data-stu-id="91ada-211">0x13</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-212">PRINTER_NOTIFY_FIELD_CJOBS</span><span class="sxs-lookup"><span data-stu-id="91ada-212">PRINTER_NOTIFY_FIELD_CJOBS</span></span></td>
<td><span data-ttu-id="91ada-213"><strong>адвдата</strong> [0] указывает количество заданий печати, поставленных в очередь для принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-213"><strong>adwData</strong> [0] specifies the number of print jobs that have been queued for the printer.</span></span></td>
<td><span data-ttu-id="91ada-214">0x14</span><span class="sxs-lookup"><span data-stu-id="91ada-214">0x14</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span><span class="sxs-lookup"><span data-stu-id="91ada-215">PRINTER_NOTIFY_FIELD_AVERAGE_PPM</span></span></td>
<td><span data-ttu-id="91ada-216"><strong>адвдата</strong> [0] указывает среднее число страниц в минуту, напечатанных на принтере.</span><span class="sxs-lookup"><span data-stu-id="91ada-216"><strong>adwData</strong> [0] specifies the average number of pages per minute that have been printed on the printer.</span></span></td>
<td><span data-ttu-id="91ada-217">0x15</span><span class="sxs-lookup"><span data-stu-id="91ada-217">0x15</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span><span class="sxs-lookup"><span data-stu-id="91ada-218">PRINTER_NOTIFY_FIELD_TOTAL_PAGES</span></span></td>
<td><span data-ttu-id="91ada-219">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-219">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-220">0x16</span><span class="sxs-lookup"><span data-stu-id="91ada-220">0x16</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="91ada-221">PRINTER_NOTIFY_FIELD_PAGES_PRINTED</span></span></td>
<td><span data-ttu-id="91ada-222">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-222">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-223">0x17</span><span class="sxs-lookup"><span data-stu-id="91ada-223">0x17</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span><span class="sxs-lookup"><span data-stu-id="91ada-224">PRINTER_NOTIFY_FIELD_TOTAL_BYTES</span></span></td>
<td><span data-ttu-id="91ada-225">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-225">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-226">0x18</span><span class="sxs-lookup"><span data-stu-id="91ada-226">0x18</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span><span class="sxs-lookup"><span data-stu-id="91ada-227">PRINTER_NOTIFY_FIELD_BYTES_PRINTED</span></span></td>
<td><span data-ttu-id="91ada-228">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-228">Not supported.</span></span></td>
<td><span data-ttu-id="91ada-229">0x19</span><span class="sxs-lookup"><span data-stu-id="91ada-229">0x19</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91ada-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span><span class="sxs-lookup"><span data-stu-id="91ada-230">PRINTER_NOTIFY_FIELD_OBJECT_GUID</span></span></td>
<td><span data-ttu-id="91ada-231">Это значение задается при изменении идентификатора GUID объекта.</span><span class="sxs-lookup"><span data-stu-id="91ada-231">This is set if the object GUID changes.</span></span></td>
<td><span data-ttu-id="91ada-232">0x1A</span><span class="sxs-lookup"><span data-stu-id="91ada-232">0x1A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91ada-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="91ada-233">PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</span></span></td>
<td><span data-ttu-id="91ada-234">Это значение задается при переименовании подключения к принтеру.</span><span class="sxs-lookup"><span data-stu-id="91ada-234">This is set if the printer connection is renamed.</span></span></td>
<td><span data-ttu-id="91ada-235">0x1B</span><span class="sxs-lookup"><span data-stu-id="91ada-235">0x1B</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="91ada-236">Если член **типа** указывает \_ тип уведомления задания \_ , элемент **field** может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="91ada-236">If the **Type** member specifies JOB\_NOTIFY\_TYPE, the **Field** member can be one of the following values.</span></span>



| <span data-ttu-id="91ada-237">Поле</span><span class="sxs-lookup"><span data-stu-id="91ada-237">Field</span></span>                                    | <span data-ttu-id="91ada-238">Тип данных</span><span class="sxs-lookup"><span data-stu-id="91ada-238">Type of data</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="91ada-239">Значение</span><span class="sxs-lookup"><span data-stu-id="91ada-239">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="91ada-240">\_ \_ имя принтера для поля уведомления о \_ задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-240">JOB\_NOTIFY\_FIELD\_PRINTER\_NAME</span></span>        | <span data-ttu-id="91ada-241">**пбуф** — это указатель на строку с завершающим нулем, содержащую имя принтера, для которого задано постановка в очередь.</span><span class="sxs-lookup"><span data-stu-id="91ada-241">**pBuf** is a pointer to a null-terminated string containing the name of the printer for which the job is spooled.</span></span>                                                                                                                                      | <span data-ttu-id="91ada-242">0x00</span><span class="sxs-lookup"><span data-stu-id="91ada-242">0x00</span></span>  |
| <span data-ttu-id="91ada-243">\_ \_ \_ имя компьютера поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-243">JOB\_NOTIFY\_FIELD\_MACHINE\_NAME</span></span>        | <span data-ttu-id="91ada-244">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя компьютера, создавшего задание печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-244">**pBuf** is a pointer to a null-terminated string that specifies the name of the machine that created the print job.</span></span>                                                                                                                                    | <span data-ttu-id="91ada-245">0x01</span><span class="sxs-lookup"><span data-stu-id="91ada-245">0x01</span></span>  |
| <span data-ttu-id="91ada-246">\_ \_ \_ имя порта поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-246">JOB\_NOTIFY\_FIELD\_PORT\_NAME</span></span>           | <span data-ttu-id="91ada-247">**пбуф** — это указатель на строку, завершающуюся нулем, которая определяет порты, используемые для передачи данных на принтер.</span><span class="sxs-lookup"><span data-stu-id="91ada-247">**pBuf** is a pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="91ada-248">Если принтер подключен к нескольким портам, имена портов разделяются запятыми (например, "LPT1:, LPT2:, LPT3:").</span><span class="sxs-lookup"><span data-stu-id="91ada-248">If a printer is connected to more than one port, the names of the ports are separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span> | <span data-ttu-id="91ada-249">0x02</span><span class="sxs-lookup"><span data-stu-id="91ada-249">0x02</span></span>  |
| <span data-ttu-id="91ada-250">\_ \_ \_ имя пользователя поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-250">JOB\_NOTIFY\_FIELD\_USER\_NAME</span></span>           | <span data-ttu-id="91ada-251">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя пользователя, отправившего задание печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-251">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who sent the print job.</span></span>                                                                                                                                           | <span data-ttu-id="91ada-252">0x03</span><span class="sxs-lookup"><span data-stu-id="91ada-252">0x03</span></span>  |
| <span data-ttu-id="91ada-253">\_ \_ \_ имя уведомления поля уведомления \_ о задании</span><span class="sxs-lookup"><span data-stu-id="91ada-253">JOB\_NOTIFY\_FIELD\_NOTIFY\_NAME</span></span>         | <span data-ttu-id="91ada-254">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя пользователя, который должен получать уведомления при печати задания или при возникновении ошибки во время печати задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-254">**pBuf** is a pointer to a null-terminated string that specifies the name of the user who should be notified when the job has been printed or when an error occurs while printing the job.</span></span>                                                              | <span data-ttu-id="91ada-255">0x04</span><span class="sxs-lookup"><span data-stu-id="91ada-255">0x04</span></span>  |
| <span data-ttu-id="91ada-256">\_ \_ тип данных поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-256">JOB\_NOTIFY\_FIELD\_DATATYPE</span></span>             | <span data-ttu-id="91ada-257">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает тип данных, используемых для записи задания печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-257">**pBuf** is a pointer to a null-terminated string that specifies the type of data used to record the print job.</span></span>                                                                                                                                         | <span data-ttu-id="91ada-258">0x05</span><span class="sxs-lookup"><span data-stu-id="91ada-258">0x05</span></span>  |
| <span data-ttu-id="91ada-259">\_ \_ \_ обработчик печати поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-259">JOB\_NOTIFY\_FIELD\_PRINT\_PROCESSOR</span></span>     | <span data-ttu-id="91ada-260">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя обработчика печати, который будет использоваться для печати задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-260">**pBuf** is a pointer to a null-terminated string that specifies the name of the print processor to be used to print the job.</span></span>                                                                                                                           | <span data-ttu-id="91ada-261">0x06</span><span class="sxs-lookup"><span data-stu-id="91ada-261">0x06</span></span>  |
| <span data-ttu-id="91ada-262">\_Параметры поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-262">JOB\_NOTIFY\_FIELD\_PARAMETERS</span></span>           | <span data-ttu-id="91ada-263">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает параметры печати-обработчика.</span><span class="sxs-lookup"><span data-stu-id="91ada-263">**pBuf** is a pointer to a null-terminated string that specifies print-processor parameters.</span></span>                                                                                                                                                            | <span data-ttu-id="91ada-264">0x07</span><span class="sxs-lookup"><span data-stu-id="91ada-264">0x07</span></span>  |
| <span data-ttu-id="91ada-265">\_ \_ \_ имя драйвера поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-265">JOB\_NOTIFY\_FIELD\_DRIVER\_NAME</span></span>         | <span data-ttu-id="91ada-266">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя драйвера принтера, который должен использоваться для обработки задания печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-266">**pBuf** is a pointer to a null-terminated string that specifies the name of the printer driver that should be used to process the print job.</span></span>                                                                                                           | <span data-ttu-id="91ada-267">0x08</span><span class="sxs-lookup"><span data-stu-id="91ada-267">0x08</span></span>  |
| <span data-ttu-id="91ada-268">\_поле уведомления о задании \_ \_ DEVMODE</span><span class="sxs-lookup"><span data-stu-id="91ada-268">JOB\_NOTIFY\_FIELD\_DEVMODE</span></span>              | <span data-ttu-id="91ada-269">**пбуф** — это указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая содержит данные об инициализации устройства и среде для драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="91ada-269">**pBuf** is a pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains device-initialization and environment data for the printer driver.</span></span>                                                                                                        | <span data-ttu-id="91ada-270">0x09</span><span class="sxs-lookup"><span data-stu-id="91ada-270">0x09</span></span>  |
| <span data-ttu-id="91ada-271">\_состояние поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-271">JOB\_NOTIFY\_FIELD\_STATUS</span></span>               | <span data-ttu-id="91ada-272">**адвдата** \[ 0 \] указывает состояние задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-272">**adwData** \[0\] specifies the job status.</span></span> <span data-ttu-id="91ada-273">Список возможных значений см. в разделе Структура [**\_ сведений о задании \_ 2**](job-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="91ada-273">For a list of possible values, see the [**JOB\_INFO\_2**](job-info-2.md) structure.</span></span>                                                                                                                        | <span data-ttu-id="91ada-274">0x0A</span><span class="sxs-lookup"><span data-stu-id="91ada-274">0x0A</span></span>  |
| <span data-ttu-id="91ada-275">\_ \_ \_ строка состояния поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-275">JOB\_NOTIFY\_FIELD\_STATUS\_STRING</span></span>       | <span data-ttu-id="91ada-276">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает состояние задания печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-276">**pBuf** is a pointer to a null-terminated string that specifies the status of the print job.</span></span>                                                                                                                                                           | <span data-ttu-id="91ada-277">0x0B</span><span class="sxs-lookup"><span data-stu-id="91ada-277">0x0B</span></span>  |
| <span data-ttu-id="91ada-278">\_ \_ \_ дескриптор безопасности поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-278">JOB\_NOTIFY\_FIELD\_SECURITY\_DESCRIPTOR</span></span> | <span data-ttu-id="91ada-279">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="91ada-279">Not supported.</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="91ada-280">0x0C</span><span class="sxs-lookup"><span data-stu-id="91ada-280">0x0C</span></span>  |
| <span data-ttu-id="91ada-281">\_документ поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-281">JOB\_NOTIFY\_FIELD\_DOCUMENT</span></span>             | <span data-ttu-id="91ada-282">**пбуф** — это указатель на строку, завершающуюся нулем, которая указывает имя задания печати (например, MS-WORD: Review.doc).</span><span class="sxs-lookup"><span data-stu-id="91ada-282">**pBuf** is a pointer to a null-terminated string that specifies the name of the print job (for example, "MS-WORD: Review.doc").</span></span>                                                                                                                        | <span data-ttu-id="91ada-283">0x0D</span><span class="sxs-lookup"><span data-stu-id="91ada-283">0x0D</span></span>  |
| <span data-ttu-id="91ada-284">\_приоритет поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-284">JOB\_NOTIFY\_FIELD\_PRIORITY</span></span>             | <span data-ttu-id="91ada-285">**адвдата** \[ 0 \] указывает приоритет задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-285">**adwData** \[0\] specifies the job priority.</span></span>                                                                                                                                                                                                           | <span data-ttu-id="91ada-286">0x0E</span><span class="sxs-lookup"><span data-stu-id="91ada-286">0x0E</span></span>  |
| <span data-ttu-id="91ada-287">\_должность поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-287">JOB\_NOTIFY\_FIELD\_POSITION</span></span>             | <span data-ttu-id="91ada-288">**адвдата** \[ 0 \] указывает расположение задания в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="91ada-288">**adwData** \[0\] specifies the job's position in the print queue.</span></span>                                                                                                                                                                                      | <span data-ttu-id="91ada-289">0x0F</span><span class="sxs-lookup"><span data-stu-id="91ada-289">0x0F</span></span>  |
| <span data-ttu-id="91ada-290">\_ \_ отправленное поле уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-290">JOB\_NOTIFY\_FIELD\_SUBMITTED</span></span>            | <span data-ttu-id="91ada-291">**пбуф** — это указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , указывающий время отправки задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-291">**pBuf** is a pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that specifies the time when the job was submitted.</span></span>                                                                                                                          | <span data-ttu-id="91ada-292">0x10</span><span class="sxs-lookup"><span data-stu-id="91ada-292">0x10</span></span>  |
| <span data-ttu-id="91ada-293">\_ \_ \_ время начала поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-293">JOB\_NOTIFY\_FIELD\_START\_TIME</span></span>          | <span data-ttu-id="91ada-294">**адвдата** \[ 0 \] указывает самое раннее время, когда задание может быть напечатано.</span><span class="sxs-lookup"><span data-stu-id="91ada-294">**adwData** \[0\] specifies the earliest time that the job can be printed.</span></span> <span data-ttu-id="91ada-295">(Это значение указывается в минутах, истекшем с 12:00 утра)</span><span class="sxs-lookup"><span data-stu-id="91ada-295">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                | <span data-ttu-id="91ada-296">0x11</span><span class="sxs-lookup"><span data-stu-id="91ada-296">0x11</span></span>  |
| <span data-ttu-id="91ada-297">\_поле уведомления о задании \_ \_ до \_ времени</span><span class="sxs-lookup"><span data-stu-id="91ada-297">JOB\_NOTIFY\_FIELD\_UNTIL\_TIME</span></span>          | <span data-ttu-id="91ada-298">**адвдата** \[ 0 \] указывает последнее время, когда задание может быть напечатано.</span><span class="sxs-lookup"><span data-stu-id="91ada-298">**adwData** \[0\] specifies the latest time that the job can be printed.</span></span> <span data-ttu-id="91ada-299">(Это значение указывается в минутах, истекшем с 12:00 утра)</span><span class="sxs-lookup"><span data-stu-id="91ada-299">(This value is specified in minutes elapsed since 12:00 A.M.)</span></span>                                                                                                                  | <span data-ttu-id="91ada-300">0x12</span><span class="sxs-lookup"><span data-stu-id="91ada-300">0x12</span></span>  |
| <span data-ttu-id="91ada-301">\_время поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-301">JOB\_NOTIFY\_FIELD\_TIME</span></span>                 | <span data-ttu-id="91ada-302">**адвдата** \[ 0 \] указывает общее время в секундах, прошедшее с момента начала печати задания.</span><span class="sxs-lookup"><span data-stu-id="91ada-302">**adwData** \[0\] specifies the total time, in seconds, that has elapsed since the job began printing.</span></span>                                                                                                                                                  | <span data-ttu-id="91ada-303">0x13</span><span class="sxs-lookup"><span data-stu-id="91ada-303">0x13</span></span>  |
| <span data-ttu-id="91ada-304">\_ \_ \_ Общее число страниц в поле уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-304">JOB\_NOTIFY\_FIELD\_TOTAL\_PAGES</span></span>         | <span data-ttu-id="91ada-305">**адвдата** \[ 0 \] задает размер задания на страницах.</span><span class="sxs-lookup"><span data-stu-id="91ada-305">**adwData** \[0\] specifies the size, in pages, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="91ada-306">0x14</span><span class="sxs-lookup"><span data-stu-id="91ada-306">0x14</span></span>  |
| <span data-ttu-id="91ada-307">\_ \_ \_ напечатанные страницы полей уведомления о заданиях \_</span><span class="sxs-lookup"><span data-stu-id="91ada-307">JOB\_NOTIFY\_FIELD\_PAGES\_PRINTED</span></span>       | <span data-ttu-id="91ada-308">**адвдата** \[ 0 \] указывает число напечатанных страниц.</span><span class="sxs-lookup"><span data-stu-id="91ada-308">**adwData** \[0\] specifies the number of pages that have printed.</span></span>                                                                                                                                                                                      | <span data-ttu-id="91ada-309">0x15</span><span class="sxs-lookup"><span data-stu-id="91ada-309">0x15</span></span>  |
| <span data-ttu-id="91ada-310">\_Общее число \_ байт для поля уведомления о задании \_ \_</span><span class="sxs-lookup"><span data-stu-id="91ada-310">JOB\_NOTIFY\_FIELD\_TOTAL\_BYTES</span></span>         | <span data-ttu-id="91ada-311">**адвдата** \[ 0 \] задает размер задания (в байтах).</span><span class="sxs-lookup"><span data-stu-id="91ada-311">**adwData** \[0\] specifies the size, in bytes, of the job.</span></span>                                                                                                                                                                                             | <span data-ttu-id="91ada-312">0x16</span><span class="sxs-lookup"><span data-stu-id="91ada-312">0x16</span></span>  |
| <span data-ttu-id="91ada-313">\_ \_ \_ число напечатанных байтов для поля уведомления о задании \_</span><span class="sxs-lookup"><span data-stu-id="91ada-313">JOB\_NOTIFY\_FIELD\_BYTES\_PRINTED</span></span>       | <span data-ttu-id="91ada-314">**адвдата** \[ 0 \] указывает число байтов, которые были распечатаны в этом задании.</span><span class="sxs-lookup"><span data-stu-id="91ada-314">**adwData** \[0\] specifies the number of bytes that have been printed on this job.</span></span> <span data-ttu-id="91ada-315">Для этого поля объект уведомления об изменении получает сигнал при отправке байтов на принтер.</span><span class="sxs-lookup"><span data-stu-id="91ada-315">For this field, the change notification object is signaled when bytes are sent to the printer.</span></span>                                                                      | <span data-ttu-id="91ada-316">0x17</span><span class="sxs-lookup"><span data-stu-id="91ada-316">0x17</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="91ada-317">Требования</span><span class="sxs-lookup"><span data-stu-id="91ada-317">Requirements</span></span>



| <span data-ttu-id="91ada-318">Требование</span><span class="sxs-lookup"><span data-stu-id="91ada-318">Requirement</span></span> | <span data-ttu-id="91ada-319">Значение</span><span class="sxs-lookup"><span data-stu-id="91ada-319">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ada-320">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91ada-320">Minimum supported client</span></span><br/> | <span data-ttu-id="91ada-321">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91ada-321">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="91ada-322">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91ada-322">Minimum supported server</span></span><br/> | <span data-ttu-id="91ada-323">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91ada-323">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91ada-324">Заголовок</span><span class="sxs-lookup"><span data-stu-id="91ada-324">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ada-325"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91ada-325"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ada-326">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91ada-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ada-327">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="91ada-327">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="91ada-328">Структуры API диспетчера очереди печати</span><span class="sxs-lookup"><span data-stu-id="91ada-328">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="91ada-329">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="91ada-329">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="91ada-330">**финднекстпринтерчанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="91ada-330">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="91ada-331">**\_Сведения о задании \_ 2**</span><span class="sxs-lookup"><span data-stu-id="91ada-331">**JOB\_INFO\_2**</span></span>](job-info-2.md)
</dt> <dt>

[<span data-ttu-id="91ada-332">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="91ada-332">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="91ada-333">**\_сведения об уведомлении принтера \_**</span><span class="sxs-lookup"><span data-stu-id="91ada-333">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="91ada-334">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="91ada-334">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="91ada-335">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="91ada-335">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

