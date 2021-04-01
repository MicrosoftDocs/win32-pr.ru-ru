---
description: Лампы на телефонном устройстве могут быть освещены в различных режимах освещения.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Ламп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081318"
---
# <a name="lamps"></a><span data-ttu-id="7ef94-103">Ламп</span><span class="sxs-lookup"><span data-stu-id="7ef94-103">Lamps</span></span>

<span data-ttu-id="7ef94-104">Лампы на телефонном устройстве могут быть освещены в различных режимах освещения.</span><span class="sxs-lookup"><span data-stu-id="7ef94-104">The lamps on a phone device can be lit in a variety of different lighting modes.</span></span> <span data-ttu-id="7ef94-105">В отличие от шаблонов для звонков, режимы лампы являются более универсальными по отношению к телефонным наборам различных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="7ef94-105">Unlike ringing patterns, lamp modes are more uniform across phone sets of different vendors.</span></span> <span data-ttu-id="7ef94-106">Общий набор режимов лампы определяется API.</span><span class="sxs-lookup"><span data-stu-id="7ef94-106">A common set of lamp modes is defined by the API.</span></span> <span data-ttu-id="7ef94-107">Лампа, определяемая ее идентификатором кнопки лампы, может быть освещена в заданном режиме лампы.</span><span class="sxs-lookup"><span data-stu-id="7ef94-107">A lamp identified by its lamp-button identifier can be lit in a given lamp mode.</span></span> <span data-ttu-id="7ef94-108">На лампу также можно запрашивать текущий режим лампы.</span><span class="sxs-lookup"><span data-stu-id="7ef94-108">A lamp can also be queried for its current lamp mode.</span></span>

<span data-ttu-id="7ef94-109">Функции TAPI, используемые для ламп, — это [**фонесетламп**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), которые перекрывают лампу на заданном открытом устройстве в заданном режиме освещения лампы, и [**фонежетламп**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), который возвращает текущий режим лампы указанной лампы.</span><span class="sxs-lookup"><span data-stu-id="7ef94-109">The TAPI functions used for lamps are [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), which lights a lamp on a specified open phone device in a given lamp lighting mode, and [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), which returns the current lamp mode of the specified lamp.</span></span>

<span data-ttu-id="7ef94-110">При изменении лампы телефонного устройства в приложение отправляется сообщение [**о \_ состоянии телефона**](phone-state.md) , чтобы уведомить приложение об изменении состояния.</span><span class="sxs-lookup"><span data-stu-id="7ef94-110">When a lamp of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="7ef94-111">Параметры этого сообщения содержат сведения об изменении.</span><span class="sxs-lookup"><span data-stu-id="7ef94-111">Parameters to this message provide an indication of the change.</span></span>

 

 



