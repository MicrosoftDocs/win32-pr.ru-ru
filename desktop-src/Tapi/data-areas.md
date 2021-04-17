---
description: Некоторые наборы телефонов поддерживают понятие загрузки или передачи данных на телефонное устройство, что позволяет программировать набор телефонов различными способами.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Области данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673720"
---
# <a name="data-areas"></a><span data-ttu-id="bbb87-103">Области данных</span><span class="sxs-lookup"><span data-stu-id="bbb87-103">Data Areas</span></span>

<span data-ttu-id="bbb87-104">Некоторые наборы телефонов поддерживают понятие загрузки или передачи данных на телефонное устройство, что позволяет программировать набор телефонов различными способами.</span><span class="sxs-lookup"><span data-stu-id="bbb87-104">Some phone sets support the notion of downloading data from or uploading data to the phone device, which allows the phone set to be programmed in a variety of ways.</span></span> <span data-ttu-id="bbb87-105">TAPI моделирует эти наборы телефонов как одну или несколько областей скачивания или отправки.</span><span class="sxs-lookup"><span data-stu-id="bbb87-105">TAPI models these phone sets as having one or more download or upload areas.</span></span> <span data-ttu-id="bbb87-106">Каждая область идентифицируется по номеру, который находится в диапазоне от нуля до количества областей данных, доступных на телефоне минус единица.</span><span class="sxs-lookup"><span data-stu-id="bbb87-106">Each area is identified by a number that ranges from zero to the number of data areas available on the phone minus one.</span></span> <span data-ttu-id="bbb87-107">Размеры каждой области могут различаться.</span><span class="sxs-lookup"><span data-stu-id="bbb87-107">Sizes of each area can vary.</span></span> <span data-ttu-id="bbb87-108">Формат самих данных зависит от конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="bbb87-108">The format of the data itself is device-specific.</span></span>

<span data-ttu-id="bbb87-109">Функция [**ФОНЕСЕТДАТА**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) TAPI загружает буфер данных в заданную область данных на телефонном устройстве, а функция [**фонежетдата**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) передает содержимое заданной области данных на телефонном устройстве в буфер.</span><span class="sxs-lookup"><span data-stu-id="bbb87-109">The TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) function downloads a buffer of data to a given data area in the phone device, and the [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) function uploads the contents of a given data area in the phone device to a buffer.</span></span>

<span data-ttu-id="bbb87-110">При изменении области данных телефонного устройства в приложение отправляется сообщение [**о \_ состоянии телефона**](phone-state.md) , чтобы уведомить приложение об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="bbb87-110">When a data area of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="bbb87-111">Параметры этого сообщения содержат сведения об изменении.</span><span class="sxs-lookup"><span data-stu-id="bbb87-111">Parameters to this message provide an indication of the change.</span></span>

 

 



