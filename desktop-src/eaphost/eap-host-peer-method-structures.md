---
title: Структуры одноранговых методов EAPHost
description: Сведения о структурах API одноранговых методов EAPHost, таких как Еапцертификатекредентиал и Еапсимкредентиал.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691666"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="2befd-103">Структуры одноранговых методов EAPHost</span><span class="sxs-lookup"><span data-stu-id="2befd-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="2befd-104">Ниже приведены структуры API одноранговых методов EAPHost.</span><span class="sxs-lookup"><span data-stu-id="2befd-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="2befd-105">Структура</span><span class="sxs-lookup"><span data-stu-id="2befd-105">Structure</span></span>                                                              | <span data-ttu-id="2befd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2befd-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2befd-107">**еапцертификатекредентиал**</span><span class="sxs-lookup"><span data-stu-id="2befd-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="2befd-108">Содержит сведения о сертификате, используемом методом EAP для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2befd-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="2befd-109">**еапкредентиал**</span><span class="sxs-lookup"><span data-stu-id="2befd-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="2befd-110">Содержит сведения о типе учетных данных и соответствующих учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2befd-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="2befd-111">Он передается в качестве входных данных в API [**еаппиржетконфигблобандусерблоб**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) .</span><span class="sxs-lookup"><span data-stu-id="2befd-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="2befd-112">**\_подпрограммы метода одноранговых \_ методов EAP \_**</span><span class="sxs-lookup"><span data-stu-id="2befd-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="2befd-113">Содержит набор указателей на функции API однорангового метода EAPHost.</span><span class="sxs-lookup"><span data-stu-id="2befd-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="2befd-114">**еаппирмесодаутпут**</span><span class="sxs-lookup"><span data-stu-id="2befd-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="2befd-115">Содержит сведения о действии, возвращаемом методом однорангового узла EAP.</span><span class="sxs-lookup"><span data-stu-id="2befd-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="2befd-116">**еаппирмесодресулт**</span><span class="sxs-lookup"><span data-stu-id="2befd-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="2befd-117">Содержит результирующие данные, созданные методом EAP во время проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2befd-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="2befd-118">**еапсимкредентиал**</span><span class="sxs-lookup"><span data-stu-id="2befd-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="2befd-119">Содержит сведения о SIM-карте, используемой методом EAP для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2befd-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="2befd-120">**еапусернамепассвордкредентиал**</span><span class="sxs-lookup"><span data-stu-id="2befd-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="2befd-121">Содержит имя пользователя и пароль, используемые методом EAP для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="2befd-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




