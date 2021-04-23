---
title: Идлеон, свойство
description: Идлеон, свойство
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328195"
---
# <a name="idleon-property"></a><span data-ttu-id="af1c2-103">Идлеон, свойство</span><span class="sxs-lookup"><span data-stu-id="af1c2-103">IdleOn Property</span></span>

<span data-ttu-id="af1c2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af1c2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af1c2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="af1c2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af1c2-106">Возвращает или задает логическое значение, определяющее, управляет ли сервер **состояние простоя** анимацией состояния для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="af1c2-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="af1c2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="af1c2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="af1c2-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Идлеон* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="af1c2-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="af1c2-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="af1c2-109">Part</span></span>      | <span data-ttu-id="af1c2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="af1c2-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af1c2-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="af1c2-111">*boolean*</span></span> | <span data-ttu-id="af1c2-112">Логическое выражение, указывающее, управляет ли сервер режимом простоя.</span><span class="sxs-lookup"><span data-stu-id="af1c2-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="af1c2-113">**True** (по умолчанию) Обработка состояния простоя сервера включена.</span><span class="sxs-lookup"><span data-stu-id="af1c2-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="af1c2-114">**Значение false** Обработка состояния простоя сервера отключена.</span><span class="sxs-lookup"><span data-stu-id="af1c2-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="af1c2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af1c2-115">Remarks</span></span>

<span data-ttu-id="af1c2-116">Сервер автоматически устанавливает время ожидания после последней анимации для символа.</span><span class="sxs-lookup"><span data-stu-id="af1c2-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="af1c2-117">По завершении этого интервала времени сервер начинает **состояние простоя** состояние символа, **состояние простоя** его анимацию с регулярными интервалами.</span><span class="sxs-lookup"><span data-stu-id="af1c2-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="af1c2-118">Если вы хотите отключить сервер от автоматического воспроизведения анимации состояния **состояние простоя** , установите свойство в **значение false** и Воспроизведите анимацию или вызовите метод [**остановите**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="af1c2-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="af1c2-119">Установка этого значения не влияет на текущее состояние анимации символа.</span><span class="sxs-lookup"><span data-stu-id="af1c2-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="af1c2-120">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="af1c2-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





