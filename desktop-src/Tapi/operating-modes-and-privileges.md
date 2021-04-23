---
description: Приложение может запросить один из двух режимов работы при открытии телефонного устройства.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Режимы работы и привилегии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba1cc01ed0552762ac3bc97449b1ae5a923cb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812490"
---
# <a name="operating-modes-and-privileges"></a><span data-ttu-id="434f5-103">Режимы работы и привилегии</span><span class="sxs-lookup"><span data-stu-id="434f5-103">Operating Modes and Privileges</span></span>

<span data-ttu-id="434f5-104">Приложение может запросить один из двух режимов работы при открытии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="434f5-104">The application can request one of two operating modes when opening a phone device.</span></span> <span data-ttu-id="434f5-105">Эти режимы соответствуют привилегиям, запрашиваемым приложением для устройства.</span><span class="sxs-lookup"><span data-stu-id="434f5-105">These modes reflect the privileges the application requests for the device:</span></span>

-   <span data-ttu-id="434f5-106">Открытие телефона для прав монитора позволяет приложению определить состояние телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="434f5-106">Opening a phone for monitor privileges lets the application determine the status of the phone device.</span></span> <span data-ttu-id="434f5-107">Сообщения отправляются в приложение при обнаружении изменений состояния на телефонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="434f5-107">Messages are sent to the application when status changes on the phone device are detected.</span></span>
-   <span data-ttu-id="434f5-108">Приложение, которое открывает телефонное устройство для привилегий владельца, может использовать операции, изменяющие состояние телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="434f5-108">An application that opens a phone device for owner privileges can use operations that modify the state of the phone device.</span></span> <span data-ttu-id="434f5-109">Права владельца автоматически включают также полный доступ к монитору.</span><span class="sxs-lookup"><span data-stu-id="434f5-109">Owner privilege automatically includes full monitor privileges as well.</span></span> <span data-ttu-id="434f5-110">Данное телефонное устройство можно открыть в любое время только один раз для привилегий владельца, но несколько раз для прав монитора.</span><span class="sxs-lookup"><span data-stu-id="434f5-110">At any time, a given phone device can be open only once for owner privileges, but multiple times for monitor privileges.</span></span> <span data-ttu-id="434f5-111">Для всех операций с **телефоном** требуются права владельца, в то время как все операции **фонежет** требуют только привилегий монитора.</span><span class="sxs-lookup"><span data-stu-id="434f5-111">All **phoneSet** operations require owner privileges, while all **phoneGet** operations require only monitor privileges.</span></span>

 

 



