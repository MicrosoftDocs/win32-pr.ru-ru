---
description: В центре безопасности Windows используются следующие функции.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Функции центра безопасности Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895333"
---
# <a name="windows-security-center-functions"></a><span data-ttu-id="bffc8-103">Функции центра безопасности Windows</span><span class="sxs-lookup"><span data-stu-id="bffc8-103">Windows Security Center Functions</span></span>

<span data-ttu-id="bffc8-104">В центре безопасности Windows используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="bffc8-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bffc8-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bffc8-105">In this section</span></span>



| <span data-ttu-id="bffc8-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="bffc8-106">Topic</span></span>                                                                           | <span data-ttu-id="bffc8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bffc8-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bffc8-108">**вскжетсекуритипровидерхеалс**</span><span class="sxs-lookup"><span data-stu-id="bffc8-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="bffc8-109">Возвращает совокупное состояние работоспособности категорий поставщиков безопасности, представленных указанными значениями [**перечисления \_ \_ поставщика безопасности WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) .</span><span class="sxs-lookup"><span data-stu-id="bffc8-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="bffc8-110">**вскрегистерфорчанжес**</span><span class="sxs-lookup"><span data-stu-id="bffc8-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="bffc8-111">Регистрирует функцию обратного вызова, которая должна выполняться, когда центр безопасности Windows (WSC) обнаруживает изменение, которое может повлиять на работоспособность одного из поставщиков безопасности.</span><span class="sxs-lookup"><span data-stu-id="bffc8-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="bffc8-112">**вскунрегистерчанжес**</span><span class="sxs-lookup"><span data-stu-id="bffc8-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="bffc8-113">Отменяет регистрацию обратного вызова, созданную путем вызова функции [**вскрегистерфорчанжес**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .</span><span class="sxs-lookup"><span data-stu-id="bffc8-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




