---
description: Используйте ведение журнала событий для записи ошибок, возникающих в библиотеке DLL производительности.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Обработка ошибок в библиотеке DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998524"
---
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="f3c98-103">Обработка ошибок в библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="f3c98-103">Error Handling in the DLL</span></span>

<span data-ttu-id="f3c98-104">Используйте ведение журнала событий для записи ошибок, возникающих в библиотеке DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="f3c98-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="f3c98-105">Ведение журнала событий ошибок помогает в устранении неполадок в приложениях, которые предоставляют данные о производительности во время разработки и после установки.</span><span class="sxs-lookup"><span data-stu-id="f3c98-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="f3c98-106">Необходимо ограничить количество записей об ошибках, возникающих в функции [**коллектперформанцедата**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , поскольку сбор данных может быть частым.</span><span class="sxs-lookup"><span data-stu-id="f3c98-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="f3c98-107">Система регистрирует следующие ошибки в журнале событий при возникновении проблем с функцией [**опенперформанцедата**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f3c98-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="f3c98-108">При возникновении одной из следующих ошибок система не вызывает библиотеку DLL производительности снова.</span><span class="sxs-lookup"><span data-stu-id="f3c98-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="f3c98-109">Вместо этого библиотека DLL выгружается.</span><span class="sxs-lookup"><span data-stu-id="f3c98-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="f3c98-110">**PERFLIB \_ ОТКРЫТАЯ \_ процедура \_ не \_ найдена**— заносится в журнал, если имя процедуры, определенное в реестре, не найдено в библиотеке DLL как экспортированная функция.</span><span class="sxs-lookup"><span data-stu-id="f3c98-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="f3c98-111">Обычно это происходит в том случае, если библиотека DLL или служба установлены неправильно или имя функции было переименовано без обновления процедуры установки.</span><span class="sxs-lookup"><span data-stu-id="f3c98-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="f3c98-112">**PERFLIB \_ Ошибка \_ Open \_ proc**— заносится в журнал, когда процедура открытия вернула состояние ошибки, отличное от Error \_ .</span><span class="sxs-lookup"><span data-stu-id="f3c98-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="f3c98-113">В этом случае библиотека DLL должна также содержать запись журнала событий, описывающую условия, вызвавшие сбой.</span><span class="sxs-lookup"><span data-stu-id="f3c98-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="f3c98-114">**PERFLIB \_ \_ \_ Исключение Open proc**— регистрируется, когда процедура открытия обнаруживает необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="f3c98-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="f3c98-115">Обычно это происходит из-за непредвиденной ошибки, возникшей при выполнении процедуры Open.</span><span class="sxs-lookup"><span data-stu-id="f3c98-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
