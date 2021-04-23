---
description: Задает заголовок и подзаголовок, которые отображаются в заголовке мастера. В общем случае клиент отобразит заголовок над HTML и под заголовком окна.
title: Вебвизардхост. Сесеадертекст, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985788"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="ea9fe-104">Вебвизардхост. Сесеадертекст, метод</span><span class="sxs-lookup"><span data-stu-id="ea9fe-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="ea9fe-105">Задает заголовок и подзаголовок, которые отображаются в заголовке мастера.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="ea9fe-106">В общем случае клиент отобразит заголовок над HTML и под заголовком окна.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea9fe-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="ea9fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea9fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9fe-109">*бстрхеадертитле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea9fe-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9fe-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ea9fe-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ea9fe-111">Строка, содержащая заголовок.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="ea9fe-112">*бстрхеадерсубтитле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ea9fe-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea9fe-113">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ea9fe-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ea9fe-114">Строка, содержащая подзаголовок.</span><span class="sxs-lookup"><span data-stu-id="ea9fe-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea9fe-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ea9fe-115">Requirements</span></span>



| <span data-ttu-id="ea9fe-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ea9fe-116">Requirement</span></span> | <span data-ttu-id="ea9fe-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ea9fe-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9fe-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea9fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9fe-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ea9fe-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea9fe-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea9fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9fe-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea9fe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea9fe-122">Header</span><span class="sxs-lookup"><span data-stu-id="ea9fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9fe-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9fe-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea9fe-124">IDL</span><span class="sxs-lookup"><span data-stu-id="ea9fe-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea9fe-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea9fe-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
