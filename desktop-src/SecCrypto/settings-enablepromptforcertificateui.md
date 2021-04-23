---
description: Задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Свойство Settings. Енаблепромптфорцертификатеуи
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688962"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="d54cf-103">Свойство Settings. Енаблепромптфорцертификатеуи</span><span class="sxs-lookup"><span data-stu-id="d54cf-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="d54cf-104">\[Свойство **енаблепромптфорцертификатеуи** доступно для использования в операционных системах, указанных в разделе требования.\]</span><span class="sxs-lookup"><span data-stu-id="d54cf-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="d54cf-105">Свойство **енаблепромптфорцертификатеуи** задает или получает логическое значение, указывающее, можно ли использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.</span><span class="sxs-lookup"><span data-stu-id="d54cf-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="d54cf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d54cf-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d54cf-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d54cf-107">Property value</span></span>

<span data-ttu-id="d54cf-108">Если **значение — true**, можно использовать пользовательский интерфейс для идентификации лица или удостоверения отправителя.</span><span class="sxs-lookup"><span data-stu-id="d54cf-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="d54cf-109">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d54cf-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="d54cf-110">Задание этого свойства не отключает предупреждения, которые генерируются до того, как использование закрытого ключа выполняется из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d54cf-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d54cf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d54cf-111">Requirements</span></span>



| <span data-ttu-id="d54cf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d54cf-112">Requirement</span></span> | <span data-ttu-id="d54cf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d54cf-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d54cf-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d54cf-114">Redistributable</span></span><br/> | <span data-ttu-id="d54cf-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d54cf-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d54cf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d54cf-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="d54cf-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d54cf-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54cf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d54cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54cf-119">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="d54cf-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




