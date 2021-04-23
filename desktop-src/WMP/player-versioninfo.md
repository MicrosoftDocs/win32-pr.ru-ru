---
title: Player. versionInfo
description: Свойство versionInfo извлекает строковое значение, указывающее версию проигрывателя Windows Media.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- Проигрыватель проигрывателя Windows Media Player. versionInfo
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44a94fa2df6d5e7d46108ec971fd84481688eb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704337"
---
# <a name="playerversioninfo"></a><span data-ttu-id="d4a99-104">Player. versionInfo</span><span class="sxs-lookup"><span data-stu-id="d4a99-104">Player.versionInfo</span></span>

<span data-ttu-id="d4a99-105">Свойство **versionInfo** извлекает строковое значение, указывающее версию проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4a99-105">The **versionInfo** property retrieves a String value specifying the version of the Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a99-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4a99-106">Syntax</span></span>

<span data-ttu-id="d4a99-107">*проигрыватель* . **versionInfo**</span><span class="sxs-lookup"><span data-stu-id="d4a99-107">*player* .**versionInfo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d4a99-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d4a99-108">Possible Values</span></span>

<span data-ttu-id="d4a99-109">Это свойство является **строкой** только для чтения в следующем формате: "*X*. 0,0. *Yyyy*"где *X* представляет основной номер версии, а *yyyy* — номер сборки.</span><span class="sxs-lookup"><span data-stu-id="d4a99-109">This property is a read-only **String** in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="d4a99-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="d4a99-110">Examples</span></span>

<span data-ttu-id="d4a99-111">В следующем примере создается HTML-элемент BUTTON, при щелчке которого отображается окно сообщения, содержащее сведения о версии проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d4a99-111">The following example creates an HTML BUTTON element that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="d4a99-112">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="d4a99-112">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a><span data-ttu-id="d4a99-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d4a99-113">Requirements</span></span>



| <span data-ttu-id="d4a99-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d4a99-114">Requirement</span></span> | <span data-ttu-id="d4a99-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d4a99-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-116">Версия</span><span class="sxs-lookup"><span data-stu-id="d4a99-116">Version</span></span><br/> | <span data-ttu-id="d4a99-117">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d4a99-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4a99-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d4a99-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4a99-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a99-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4a99-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a99-121">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="d4a99-121">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





