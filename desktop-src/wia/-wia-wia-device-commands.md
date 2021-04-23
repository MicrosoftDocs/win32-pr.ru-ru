---
description: Следующие константы формируют набор допустимых команд аппаратного устройства для получения образа Windows (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Команды устройства WIA (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897434"
---
# <a name="wia-device-commands"></a><span data-ttu-id="78eb5-103">Команды устройства WIA</span><span class="sxs-lookup"><span data-stu-id="78eb5-103">WIA Device Commands</span></span>

<span data-ttu-id="78eb5-104">Следующие константы формируют набор допустимых команд аппаратного устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="78eb5-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="78eb5-105">Константа</span><span class="sxs-lookup"><span data-stu-id="78eb5-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="78eb5-106">Описание</span><span class="sxs-lookup"><span data-stu-id="78eb5-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="78eb5-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-108">Приводит к тому, что минидривер устройства синхронизируют кэшированные элементы с аппаратным устройством.</span><span class="sxs-lookup"><span data-stu-id="78eb5-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="78eb5-109">Если устройство поддерживает метод <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>ивиаитем:: анализеитем</strong></a> , выполнив эту команду, минидривер отклоняет результаты анализа и сбрасывает элемент в исходное состояние.</span><span class="sxs-lookup"><span data-stu-id="78eb5-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="78eb5-110">Все драйверы должны поддерживать эту команду.</span><span class="sxs-lookup"><span data-stu-id="78eb5-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="78eb5-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-112">Заставляет устройство WIA получить изображение.</span><span class="sxs-lookup"><span data-stu-id="78eb5-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="78eb5-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-114">Указывает устройству удалить все элементы, которые могут быть удалены из дерева объектов <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>ивиаитем</strong></a> , представляющих устройство.</span><span class="sxs-lookup"><span data-stu-id="78eb5-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="78eb5-115">Удаление элемента запрещено путем задания свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="78eb5-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="78eb5-116">Дополнительные сведения см. в разделе <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>ивиапропертистораже:: сетпропертистреам</strong></a> и <a href="-wia-property-attributes.md">атрибуты свойств</a>.</span><span class="sxs-lookup"><span data-stu-id="78eb5-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="78eb5-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-118">Используется для сканеров документов.</span><span class="sxs-lookup"><span data-stu-id="78eb5-118">Used for document scanners.</span></span> <span data-ttu-id="78eb5-119">Заставляет средство проверки загружать следующую страницу в обработчике документов.</span><span class="sxs-lookup"><span data-stu-id="78eb5-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="78eb5-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-121">Используется для сканеров документов.</span><span class="sxs-lookup"><span data-stu-id="78eb5-121">Used for document scanners.</span></span> <span data-ttu-id="78eb5-122">Указывает устройству выгружать все оставшиеся страницы в обработчике документа.</span><span class="sxs-lookup"><span data-stu-id="78eb5-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="78eb5-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-124">Используется для сканеров документов с податчиком страниц.</span><span class="sxs-lookup"><span data-stu-id="78eb5-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="78eb5-125">Указывает устройству запустить двигатель устройства подачи.</span><span class="sxs-lookup"><span data-stu-id="78eb5-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="78eb5-126">Эта функция доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78eb5-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="78eb5-127">Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="78eb5-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="78eb5-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-129">Используется для сканеров документов с податчиком страниц.</span><span class="sxs-lookup"><span data-stu-id="78eb5-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="78eb5-130">Указывает устройству на необходимость отключить двигатель устройства подачи.</span><span class="sxs-lookup"><span data-stu-id="78eb5-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="78eb5-131">Эта функция доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78eb5-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="78eb5-132">Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <strong>WIA_IPS_FEEDER_CONTROL</strong> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="78eb5-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="78eb5-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="78eb5-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="78eb5-134">Используется для сканеров документов с податчиком страниц.</span><span class="sxs-lookup"><span data-stu-id="78eb5-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="78eb5-135">Указывает устройству приостановить мотор.</span><span class="sxs-lookup"><span data-stu-id="78eb5-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="78eb5-136">Эта функция доступна начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78eb5-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="78eb5-137">Минидривер WIA должен отклонить эту команду и вернуть <strong>WIA_ERROR_INVALID_COMMAND</strong> , если свойство <strong>WIA_IPS_FEEDER_CONTROL</strong> не поддерживается или имеет значение WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="78eb5-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="78eb5-138">Требования</span><span class="sxs-lookup"><span data-stu-id="78eb5-138">Requirements</span></span>



| <span data-ttu-id="78eb5-139">Требование</span><span class="sxs-lookup"><span data-stu-id="78eb5-139">Requirement</span></span> | <span data-ttu-id="78eb5-140">Значение</span><span class="sxs-lookup"><span data-stu-id="78eb5-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78eb5-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78eb5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="78eb5-142">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="78eb5-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="78eb5-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78eb5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="78eb5-144">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78eb5-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78eb5-145">Header</span><span class="sxs-lookup"><span data-stu-id="78eb5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="78eb5-146"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="78eb5-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
