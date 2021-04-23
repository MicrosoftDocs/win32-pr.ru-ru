---
description: 'Виатрансферпарамс передается в приложение во время передачи данных системой времени выполнения Windows Image (WIA) в метод Ивиатрансферкаллбакк:: Трансферкаллбакк.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Структура Виатрансферпарамс (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692400"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="293b4-103">Структура Виатрансферпарамс</span><span class="sxs-lookup"><span data-stu-id="293b4-103">WiaTransferParams structure</span></span>

<span data-ttu-id="293b4-104">**Виатрансферпарамс** передается в приложение во время передачи данных системой времени выполнения Windows Image (WIA) в метод [**Ивиатрансферкаллбакк:: трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) .</span><span class="sxs-lookup"><span data-stu-id="293b4-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="293b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="293b4-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="293b4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="293b4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="293b4-107">**лмессаже**</span><span class="sxs-lookup"><span data-stu-id="293b4-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="293b4-108">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="293b4-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="293b4-109">Указывает состояние передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="293b4-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="293b4-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_состояние сообщений \_ \_ о переносе WIA**</span><span class="sxs-lookup"><span data-stu-id="293b4-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="293b4-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ конец \_ \_ потока сообщения передачи WIA**</span><span class="sxs-lookup"><span data-stu-id="293b4-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="293b4-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ конец \_ \_ перемещения сообщения о переносе WIA**</span><span class="sxs-lookup"><span data-stu-id="293b4-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="293b4-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_ \_ \_ состояние устройства сообщения \_ о перепереносе WIA**</span><span class="sxs-lookup"><span data-stu-id="293b4-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="293b4-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ Новая страница сообщения о переносе WIA \_**</span><span class="sxs-lookup"><span data-stu-id="293b4-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="293b4-115">**лперценткомплете**</span><span class="sxs-lookup"><span data-stu-id="293b4-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="293b4-116">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="293b4-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="293b4-117">Указывает ход выполнения операции перемещения данных в процентах.</span><span class="sxs-lookup"><span data-stu-id="293b4-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="293b4-118">**ултрансферредбитес**</span><span class="sxs-lookup"><span data-stu-id="293b4-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="293b4-119">Тип: **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="293b4-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="293b4-120">Указывает объем передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="293b4-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="293b4-121">**хреррорстатус**</span><span class="sxs-lookup"><span data-stu-id="293b4-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="293b4-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="293b4-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="293b4-123">Состояние (или состояние ошибки) устройства, установленного драйвером; Например, "прогрев".</span><span class="sxs-lookup"><span data-stu-id="293b4-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="293b4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="293b4-124">Requirements</span></span>



| <span data-ttu-id="293b4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="293b4-125">Requirement</span></span> | <span data-ttu-id="293b4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="293b4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="293b4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="293b4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="293b4-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="293b4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="293b4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="293b4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="293b4-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="293b4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="293b4-131">Header</span><span class="sxs-lookup"><span data-stu-id="293b4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="293b4-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="293b4-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




