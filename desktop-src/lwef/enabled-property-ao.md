---
title: Свойство Enabled (объект Аудиуутпут)
description: Свойство Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071022"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="1314e-103">Свойство Enabled (объект Аудиуутпут)</span><span class="sxs-lookup"><span data-stu-id="1314e-103">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="1314e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1314e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1314e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="1314e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1314e-106">Возвращает логическое значение, указывающее, включены ли выходные данные звука (речь).</span><span class="sxs-lookup"><span data-stu-id="1314e-106">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="1314e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1314e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1314e-108">*агент \* \* *. Аудиуутпут. Enabled**</span><span class="sxs-lookup"><span data-stu-id="1314e-108">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="1314e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1314e-109">Value</span></span>     | <span data-ttu-id="1314e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1314e-110">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="1314e-111">**True**</span><span class="sxs-lookup"><span data-stu-id="1314e-111">**True**</span></span>  | <span data-ttu-id="1314e-112">Параметры Включен речевой вывод.</span><span class="sxs-lookup"><span data-stu-id="1314e-112">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="1314e-113">**False**</span><span class="sxs-lookup"><span data-stu-id="1314e-113">**False**</span></span> | <span data-ttu-id="1314e-114">Речевое Выходное звуковое сопровождение отключено.</span><span class="sxs-lookup"><span data-stu-id="1314e-114">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1314e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1314e-115">Remarks</span></span>

<span data-ttu-id="1314e-116">Это свойство отражает параметр воспроизведение аудио вывода на странице вывод страницы свойств агента (дополнительные параметры символов).</span><span class="sxs-lookup"><span data-stu-id="1314e-116">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="1314e-117">Если свойство [**Enabled**](enabled-property.md) возвращает **значение true**, то метод [**говорите**](speak-method.md) создает выходные данные, если установлен совместимый обработчик TTS, или для речевого вывода используются звуковые файлы.</span><span class="sxs-lookup"><span data-stu-id="1314e-117">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="1314e-118">При возврате значения **false** это означает, что речевой вывод не установлен или отключен пользователем.</span><span class="sxs-lookup"><span data-stu-id="1314e-118">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="1314e-119">Параметр свойства применяется ко всем символам агента и доступен только для чтения; только пользователь может установить это значение свойства.</span><span class="sxs-lookup"><span data-stu-id="1314e-119">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="1314e-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="1314e-120">See Also</span></span>

[<span data-ttu-id="1314e-121">Событие Ажентпропертичанже</span><span class="sxs-lookup"><span data-stu-id="1314e-121">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




