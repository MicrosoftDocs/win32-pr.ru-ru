---
description: '\_ \_ Константы аудклнт сессионфлагс XXX указывают характеристики сеанса звука, связанного с потоком.'
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Константы AUDCLNT_SESSIONFLAGS_XXX (Аудиосессионтипес. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496695"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="2bbe7-103">\_ \_ Константы аудклнт сессионфлагс XXX</span><span class="sxs-lookup"><span data-stu-id="2bbe7-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="2bbe7-104">\_ \_ Константы аудклнт сессионфлагс XXX указывают характеристики сеанса звука, связанного с потоком.</span><span class="sxs-lookup"><span data-stu-id="2bbe7-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="2bbe7-105">Клиент может указать эти параметры во время инициализации потока с помощью параметра *стреамфлагс* метода [**Иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="2bbe7-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="2bbe7-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="2bbe7-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="2bbe7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2bbe7-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="2bbe7-108"><dt>**Аудклнт \_ СЕССИОНФЛАГС \_ експиревхенуновнед**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe7-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="2bbe7-109">Срок действия сеанса истекает, если нет связанных потоков и владеющих объектами управления сеансами ссылки.</span><span class="sxs-lookup"><span data-stu-id="2bbe7-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="2bbe7-110"><dt>**Аудклнт \_ СЕССИОНФЛАГС \_ отобразить \_ Скрыть**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe7-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="2bbe7-111">Элемент управления "Громкость" скрывается в пользовательском интерфейсе микшера громкости при создании сеанса звука.</span><span class="sxs-lookup"><span data-stu-id="2bbe7-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="2bbe7-112">Если сеанс, связанный с потоком, уже существует до того, как [**иаудиоклиент:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) откроет поток, в микшере тома появится регулятор громкости.</span><span class="sxs-lookup"><span data-stu-id="2bbe7-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="2bbe7-113"><dt> **Аудклнт \_ сессионфлагс \_ Отображение \_ хидевхенекспиред**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe7-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="2bbe7-114">После истечения срока действия сеанса элемент управления громкостью скрывается в пользовательском интерфейсе микшера тома.</span><span class="sxs-lookup"><span data-stu-id="2bbe7-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="2bbe7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2bbe7-115">Requirements</span></span>



| <span data-ttu-id="2bbe7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2bbe7-116">Requirement</span></span> | <span data-ttu-id="2bbe7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2bbe7-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bbe7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bbe7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2bbe7-119">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2bbe7-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2bbe7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bbe7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2bbe7-121">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bbe7-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bbe7-122">Header</span><span class="sxs-lookup"><span data-stu-id="2bbe7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bbe7-123"><dt>Аудиосессионтипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bbe7-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bbe7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2bbe7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bbe7-125">Константы аудиоподсистемы Core</span><span class="sxs-lookup"><span data-stu-id="2bbe7-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="2bbe7-126">**иаудиосессионконтрол**</span><span class="sxs-lookup"><span data-stu-id="2bbe7-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




