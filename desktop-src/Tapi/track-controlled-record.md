---
description: В этом разделе приводится процедура для выполнения записи звуковых потоков, контролируемых системой мониторинга.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Запись Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910307"
---
# <a name="track-controlled-record"></a><span data-ttu-id="68828-103">Запись Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="68828-103">Track-Controlled Record</span></span>

<span data-ttu-id="68828-104">В этом разделе приводится процедура для выполнения записи звуковых потоков, контролируемых системой мониторинга.</span><span class="sxs-lookup"><span data-stu-id="68828-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="68828-105">**Для выполнения записи звуковых потоков, контролируемых системой мониторинга**</span><span class="sxs-lookup"><span data-stu-id="68828-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="68828-106">Выберите файловые терминалы на потоках.</span><span class="sxs-lookup"><span data-stu-id="68828-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="68828-107">Создайте терминал записи файлов.</span><span class="sxs-lookup"><span data-stu-id="68828-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="68828-108">Задайте имя файла.</span><span class="sxs-lookup"><span data-stu-id="68828-108">Set the file name.</span></span>
4.  <span data-ttu-id="68828-109">Перечисление потоков в вызове TAPI.</span><span class="sxs-lookup"><span data-stu-id="68828-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="68828-110">Для выполнения этих действий см. следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="68828-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="68828-111">Вызовите метод [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) в терминале записи файлов, чтобы начать запись потока.</span><span class="sxs-lookup"><span data-stu-id="68828-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="68828-112">**Перечисление потоков в вызове TAPI**</span><span class="sxs-lookup"><span data-stu-id="68828-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="68828-113">Создайте дорожку с тем же типом и направлением звука, что и в потоке.</span><span class="sxs-lookup"><span data-stu-id="68828-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="68828-114">Задайте свойства дорожки для звукового формата.</span><span class="sxs-lookup"><span data-stu-id="68828-114">Set the track properties for audio format.</span></span> <span data-ttu-id="68828-115">Если не задано, формат будет таким же, как и формат потоков.</span><span class="sxs-lookup"><span data-stu-id="68828-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="68828-116">Выберите запись в потоке.</span><span class="sxs-lookup"><span data-stu-id="68828-116">Select the track on the stream.</span></span>

<span data-ttu-id="68828-117">Если в нескольких потоках выбрана одна запись, это подразумевает смешивание потоков.</span><span class="sxs-lookup"><span data-stu-id="68828-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



