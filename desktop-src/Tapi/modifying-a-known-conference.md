---
description: В следующем фрагменте кода показано изменение интервала времени конференций. Интервал времени по умолчанию составляет тридцати минут. В этом фрагменте интервал времени установлен в один год.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Изменение известной конференции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262846"
---
# <a name="modifying-a-known-conference"></a><span data-ttu-id="f7104-105">Изменение известной конференции</span><span class="sxs-lookup"><span data-stu-id="f7104-105">Modifying a Known Conference</span></span>

<span data-ttu-id="f7104-106">\[В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="f7104-106">\[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f7104-107">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f7104-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f7104-108">В следующем фрагменте кода показано изменение интервала времени Конференции.</span><span class="sxs-lookup"><span data-stu-id="f7104-108">The following code fragment illustrates modification of a conference's time span.</span></span> <span data-ttu-id="f7104-109">Интервал времени по умолчанию составляет тридцати минут.</span><span class="sxs-lookup"><span data-stu-id="f7104-109">The default time span is thirty minutes.</span></span> <span data-ttu-id="f7104-110">В этом фрагменте интервал времени установлен в один год.</span><span class="sxs-lookup"><span data-stu-id="f7104-110">In this fragment, the time span is set to one year.</span></span>

<span data-ttu-id="f7104-111">В этом фрагменте предполагается, что [Подключение к серверу ILS](connecting-to-an-ils-server.md) уже выполнено, и было выполнено [перечисление каталога конференций](enumerating-conference-directories.md) для получения записи каталога, которая будет изменена.</span><span class="sxs-lookup"><span data-stu-id="f7104-111">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed and that a [conference directory enumeration](enumerating-conference-directories.md) has been performed to obtain the directory entry that will be modified.</span></span>

<span data-ttu-id="f7104-112">Этот фрагмент также предполагает, что это не многоадресная конференция.</span><span class="sxs-lookup"><span data-stu-id="f7104-112">This fragment also assumes this is not a multicast conference.</span></span> <span data-ttu-id="f7104-113">Для изменения времени на конференции многоадресной рассылки требуется уведомление о сервере распределения адресов многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="f7104-113">Changing the times on a multicast conference requires notification of the multicast address allocation server.</span></span> <span data-ttu-id="f7104-114">Пример работы с адресацией многоадресной рассылки см. [в разделе Получение адреса многоадресной рассылки](acquiring-a-multicast-address.md) .</span><span class="sxs-lookup"><span data-stu-id="f7104-114">See [Acquiring a Multicast Address](acquiring-a-multicast-address.md) for an example of working with multicast addressing.</span></span>


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a><span data-ttu-id="f7104-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f7104-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7104-116">**итдиректорйобжектконференце**</span><span class="sxs-lookup"><span data-stu-id="f7104-116">**ITDirectoryObjectConference**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



