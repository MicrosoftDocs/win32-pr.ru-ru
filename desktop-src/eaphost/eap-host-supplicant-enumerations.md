---
title: Перечисления для запрашивающих сторона EAPHost
description: Сведения о перечислениях API-интерфейсов EAPHost, таких как Еафостпирмесодресултреасон и \_ состояние изоляции.
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891065"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="7237f-103">Перечисления для запрашивающих сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="7237f-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="7237f-104">Ниже приведены перечисления API-интерфейса EAPHost для запрашивающего устройства.</span><span class="sxs-lookup"><span data-stu-id="7237f-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="7237f-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="7237f-105">Enumeration</span></span>                                                                  | <span data-ttu-id="7237f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7237f-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7237f-107">**\_Интерактивный \_ \_ тип данных пользовательского интерфейса \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="7237f-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="7237f-108">Указывает набор типов данных контекста интерактивного пользовательского интерфейса, предоставляемых определенным вызовам API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7237f-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="7237f-109">**\_ \_ тип свойства метода \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="7237f-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="7237f-110">Windows 7 или более поздней версии: указывает тип свойства метода.</span><span class="sxs-lookup"><span data-stu-id="7237f-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="7237f-111">**\_ \_ \_ тип значения свойства метода \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="7237f-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="7237f-112">Windows 7 или более поздней версии: указывает тип данных значения свойства метода.</span><span class="sxs-lookup"><span data-stu-id="7237f-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="7237f-113">**\_состояние проверки подлинности EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="7237f-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="7237f-114">Определяет набор возможных значений состояния сеанса проверки подлинности EAP.</span><span class="sxs-lookup"><span data-stu-id="7237f-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="7237f-115">**еафостпирауспарамс**</span><span class="sxs-lookup"><span data-stu-id="7237f-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="7237f-116">Определяет набор возможных значений параметров проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7237f-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="7237f-117">**еафостпирмесодресултреасон**</span><span class="sxs-lookup"><span data-stu-id="7237f-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="7237f-118">Определяет набор возможных причин, описывающих результаты, возвращаемые методом EAP для запрашивающего.</span><span class="sxs-lookup"><span data-stu-id="7237f-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="7237f-119">**еафостпирреспонсеактион**</span><span class="sxs-lookup"><span data-stu-id="7237f-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="7237f-120">Определяет набор действий, которые метод проверки подлинности или однорангового узла EAP может указывать на вызывающий объект во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7237f-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="7237f-121">**\_состояние изоляции**</span><span class="sxs-lookup"><span data-stu-id="7237f-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="7237f-122">Определяет набор возможных значений состояния изоляции компьютера.</span><span class="sxs-lookup"><span data-stu-id="7237f-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




