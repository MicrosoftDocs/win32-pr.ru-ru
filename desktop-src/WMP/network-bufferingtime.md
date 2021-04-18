---
title: Network. Буфферингтиме
description: Свойство Буфферингтиме указывает или получает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Проигрыватель Windows Media Network. Буфферингтиме
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704212"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="ba18b-104">Network. Буфферингтиме</span><span class="sxs-lookup"><span data-stu-id="ba18b-104">Network.bufferingTime</span></span>

<span data-ttu-id="ba18b-105">Свойство **буфферингтиме** указывает или получает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ba18b-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba18b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba18b-106">Syntax</span></span>

<span data-ttu-id="ba18b-107">*проигрыватель*. *сеть*. **буфферингтиме**</span><span class="sxs-lookup"><span data-stu-id="ba18b-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ba18b-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ba18b-108">Possible Values</span></span>

<span data-ttu-id="ba18b-109">Это свойство является **числом** для чтения и записи (**длинное**) в диапазоне от нуля до 60 000 со значением по умолчанию 5 000.</span><span class="sxs-lookup"><span data-stu-id="ba18b-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="ba18b-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="ba18b-110">Examples</span></span>

<span data-ttu-id="ba18b-111">В следующем примере JScript используется *Network*. **буфферингтиме** , чтобы указать количество секунд, выделенных для буферизации входящих данных.</span><span class="sxs-lookup"><span data-stu-id="ba18b-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="ba18b-112">Сведения извлекаются из HTML-элемента ввода текста, созданного с помощью ID = "Буфтекст".</span><span class="sxs-lookup"><span data-stu-id="ba18b-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="ba18b-113">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="ba18b-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="ba18b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ba18b-114">Requirements</span></span>



| <span data-ttu-id="ba18b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ba18b-115">Requirement</span></span> | <span data-ttu-id="ba18b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ba18b-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba18b-117">Версия</span><span class="sxs-lookup"><span data-stu-id="ba18b-117">Version</span></span><br/> | <span data-ttu-id="ba18b-118">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ba18b-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ba18b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ba18b-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba18b-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba18b-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba18b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba18b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba18b-122">**Сетевой объект**</span><span class="sxs-lookup"><span data-stu-id="ba18b-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





