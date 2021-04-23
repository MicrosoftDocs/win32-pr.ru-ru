---
description: Дополнительные службы телефонии — это коллекция всех служб, определенных API, не входящих в базовый набор телефонии.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Дополнительные службы телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909608"
---
# <a name="supplementary-telephony-services"></a><span data-ttu-id="9a75d-103">Дополнительные службы телефонии</span><span class="sxs-lookup"><span data-stu-id="9a75d-103">Supplementary Telephony Services</span></span>

<span data-ttu-id="9a75d-104">Дополнительные службы телефонии — это коллекция всех служб, определенных API, не входящих в базовый набор телефонии.</span><span class="sxs-lookup"><span data-stu-id="9a75d-104">Supplementary Telephony services are the collection of all the services defined by the API other than those included in the Basic Telephony subset.</span></span> <span data-ttu-id="9a75d-105">Он включает все так называемые дополнительные функции, имеющиеся в современных УАТС, такие как удержание, перенос, Конференция, припарк и т. д.</span><span class="sxs-lookup"><span data-stu-id="9a75d-105">It includes all so-called supplementary features found on modern PBXs, such as hold, transfer, conference, park, and so on.</span></span> <span data-ttu-id="9a75d-106">Все дополнительные функции считаются необязательными. Это значит, что поставщик услуг решает, какие из этих служб она делает или не предоставляет.</span><span class="sxs-lookup"><span data-stu-id="9a75d-106">All supplementary features are considered optional; that is, the service provider decides which of these services it does or does not provide.</span></span>

<span data-ttu-id="9a75d-107">Приложение может запросить линию или телефонное устройство для набора дополнительных служб, которые он предоставляет, используя такие функции, как [**линежетдевкапс**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) или [**линежетаддресскапс**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="9a75d-107">An application can query a line or phone device for the set of supplementary services it provides using functions such as [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) or [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps).</span></span> <span data-ttu-id="9a75d-108">Одна дополнительная служба может состоять из нескольких вызовов функций и сообщений.</span><span class="sxs-lookup"><span data-stu-id="9a75d-108">A single supplementary service may consist of multiple function calls and messages.</span></span> <span data-ttu-id="9a75d-109">API телефонии, а не разработчик поставщика услуг, определяет поведение каждой из этих дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="9a75d-109">The Telephony API, and not the service provider developer, defines the behavior of each of these supplementary features.</span></span> <span data-ttu-id="9a75d-110">Поставщик услуг должен предоставлять дополнительную службу телефонии, только если он может реализовать точное значение, определенное API.</span><span class="sxs-lookup"><span data-stu-id="9a75d-110">A service provider should provide a Supplementary Telephony service only if it can implement the exact meaning as defined by the API.</span></span> <span data-ttu-id="9a75d-111">В противном случае эта функция должна быть предоставлена в качестве расширенной службы телефонии.</span><span class="sxs-lookup"><span data-stu-id="9a75d-111">If not, the feature should be provided as an Extended Telephony service.</span></span>

<span data-ttu-id="9a75d-112">Как упоминалось в основных службах телефонии, службы телефонных устройств считаются необязательными.</span><span class="sxs-lookup"><span data-stu-id="9a75d-112">As mentioned in Basic Telephony services, phone-device services are considered optional.</span></span> <span data-ttu-id="9a75d-113">Таким образом, все службы телефонных устройств являются частью дополнительной телефонии.</span><span class="sxs-lookup"><span data-stu-id="9a75d-113">Therefore, all phone-device services are part of Supplementary Telephony.</span></span> <span data-ttu-id="9a75d-114">Список функций дополнительной телефонии см. в [справочнике по быстрой функции TAPI](./tapi-quick-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a75d-114">For a list of the functions of Supplementary Telephony, see [TAPI Quick Function Reference](./tapi-quick-function-reference.md).</span></span>

 

 
