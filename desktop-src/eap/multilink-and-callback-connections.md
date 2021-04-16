---
title: Многоканальные соединения и подключения обратного вызова
description: Для первой ссылки в многоканальном соединении служба проверки подлинности устанавливает флаг RAS- \_ \_ флага \_ первой \_ ссылки в элементе ФФЛАГС в \_ \_ структуре ввода PPP EAP.
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105710221"
---
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="c8a57-103">Многоканальные соединения и подключения обратного вызова</span><span class="sxs-lookup"><span data-stu-id="c8a57-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="c8a57-104">Для первой ссылки в многоканальном соединении служба проверки подлинности устанавливает флаг RAS- \_ \_ флага \_ первой \_ ссылки в элементе **ффлагс** в структуре [**\_ \_ ввода PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) .</span><span class="sxs-lookup"><span data-stu-id="c8a57-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="c8a57-105">Протокол проверки подлинности может использовать наличие этого флага, чтобы определить, следует ли предоставлять пользовательский интерфейс специально для первой ссылки многоканального подключения.</span><span class="sxs-lookup"><span data-stu-id="c8a57-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="c8a57-106">Если подключение настроено таким образом, что сервер обращается к клиентскому компьютеру, флаг RAS- \_ \_ флага \_ первой \_ ссылки не будет установлен при обратном вызове.</span><span class="sxs-lookup"><span data-stu-id="c8a57-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="c8a57-107">Если протокол проверки подлинности устанавливает **значение true** для элемента **фсавеконнектиондата** в [**\_ \_ выходных данных PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) , последующие ссылки в многоканальном соединении получают новые данные, относящиеся к конкретному соединению.</span><span class="sxs-lookup"><span data-stu-id="c8a57-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="c8a57-108">Однако в случае данных, относящихся к пользователю, протокол проверки подлинности по-настоящему получает исходные данные пользователя, даже если он устанавливает **значение true** для элемента **фсавеусердата** в **выходных данных PPP \_ EAP \_** .</span><span class="sxs-lookup"><span data-stu-id="c8a57-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="c8a57-109">Протокол проверки подлинности может использовать [интерактивный пользовательский интерфейс](interactive-user-interface.md) для получения данных для определенной ссылки многоканального подключения.</span><span class="sxs-lookup"><span data-stu-id="c8a57-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="c8a57-110">В этом случае служба проверки подлинности делает полученные данные доступными для протокола проверки подлинности при последующих ссылках.</span><span class="sxs-lookup"><span data-stu-id="c8a57-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="c8a57-111">Однако эти данные никогда не сохраняются в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="c8a57-111">However, this data is never saved to persistent storage.</span></span>

 

 




