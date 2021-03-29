---
title: Проверка связи
description: Используйте пакет Ping для установления соединения и согласования безопасности с сервером.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Проверка связи
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105654255"
---
# <a name="ping"></a><span data-ttu-id="b700f-104">Проверка связи</span><span class="sxs-lookup"><span data-stu-id="b700f-104">Ping</span></span>

<span data-ttu-id="b700f-105">Используйте пакет **ping** для установления соединения и согласования безопасности с сервером.</span><span class="sxs-lookup"><span data-stu-id="b700f-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="b700f-106">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b700f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="b700f-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS</span><span class="sxs-lookup"><span data-stu-id="b700f-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="b700f-108">Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.</span><span class="sxs-lookup"><span data-stu-id="b700f-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="b700f-109">Замените Remote-URL абсолютным или относительным URI.</span><span class="sxs-lookup"><span data-stu-id="b700f-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="b700f-110">Обычно замените Remote-URL именем удаленного файла задания.</span><span class="sxs-lookup"><span data-stu-id="b700f-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="b700f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span><span class="sxs-lookup"><span data-stu-id="b700f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="b700f-112">Идентифицирует этот пакет запроса как пакет проверки связи.</span><span class="sxs-lookup"><span data-stu-id="b700f-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b700f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b700f-113">Remarks</span></span>

<span data-ttu-id="b700f-114">Пакет **ping** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b700f-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="b700f-115">Вместо отправки пакета **проверки связи** можно использовать пакет [**создания сеанса**](create-session.md) для установления соединения и согласования безопасности.</span><span class="sxs-lookup"><span data-stu-id="b700f-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="b700f-116">Однако для этой цели более эффективно использовать пакет **ping** .</span><span class="sxs-lookup"><span data-stu-id="b700f-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="b700f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b700f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b700f-118">**Подтверждение проверки связи**</span><span class="sxs-lookup"><span data-stu-id="b700f-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="b700f-119">**Создание сеанса**</span><span class="sxs-lookup"><span data-stu-id="b700f-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




