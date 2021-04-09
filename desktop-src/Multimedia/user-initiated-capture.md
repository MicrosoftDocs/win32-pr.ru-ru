---
title: Запись User-Initiated
description: Запись User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888860"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="ed50f-105">Запись User-Initiated</span><span class="sxs-lookup"><span data-stu-id="ed50f-105">User-Initiated Capture</span></span>

<span data-ttu-id="ed50f-106">Вы можете получить текущее значение флага записи, инициированного пользователем, с помощью сообщения [**о \_ \_ \_ \_ настройке получения закрепления WM**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="ed50f-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="ed50f-107">Значение флага хранится в элементе **фмакеусерхитоктокаптуре** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="ed50f-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="ed50f-108">Вы можете предоставить пользователю точный контроль над временем запуска сеанса записи, установив для этого члена **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ed50f-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="ed50f-109">Авикап отображает диалоговое окно после выделения всех буферов видео и аудио для сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="ed50f-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="ed50f-110">Это позволяет пользователю устранить задержки записи из-за инициализации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="ed50f-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="ed50f-111">Если приложение использует небольшое количество буферов видео, это диалоговое окно, вероятно, не требуется.</span><span class="sxs-lookup"><span data-stu-id="ed50f-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="ed50f-112">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="ed50f-112">The default value is **FALSE**.</span></span>

 

 




