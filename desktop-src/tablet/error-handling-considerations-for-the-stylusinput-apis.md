---
description: Общие сведения об обработке ошибок при использовании Стилусинпут прикладных программных интерфейсов (API).
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Рекомендации по обработке ошибок для API Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991167"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a><span data-ttu-id="2bde1-103">Рекомендации по обработке ошибок для API Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="2bde1-103">Error Handling Considerations for the StylusInput API</span></span>

<span data-ttu-id="2bde1-104">Необработанные исключения, вызванные подключаемым модулем, перехватываются объектом [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2bde1-104">Unhandled exceptions thrown by a plug-in are caught by the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="2bde1-105">Когда подключаемый модуль создает исключение, нормальный поток данных прерывается.</span><span class="sxs-lookup"><span data-stu-id="2bde1-105">When a plug-in throws an exception, the normal flow of data is interrupted.</span></span> <span data-ttu-id="2bde1-106">Объект **RealTimeStylus** :</span><span class="sxs-lookup"><span data-stu-id="2bde1-106">The **RealTimeStylus** object:</span></span>

1.  <span data-ttu-id="2bde1-107">Создает объект [ErrorData](/previous-versions/ms575221(v=vs.100)) (в управляемом коде).</span><span class="sxs-lookup"><span data-stu-id="2bde1-107">Creates an [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code).</span></span>
2.  <span data-ttu-id="2bde1-108">Вызывает метод [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (в управляемом коде — метод [Microsoft. стилусинпут. истилуссинкплугин. Error](/previous-versions/ms824754(v=msdn.10)) или [Microsoft. стилусинпут. истилусасинкплугин. Error](/previous-versions/ms824771(v=msdn.10)) ) подключаемого модуля, который вызвал исключение.</span><span class="sxs-lookup"><span data-stu-id="2bde1-108">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method (in managed code, either the [Microsoft.StylusInput.IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method) of the plug-in that threw the exception.</span></span>
3.  <span data-ttu-id="2bde1-109">Вызывает метод [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) для оставшихся подключаемых модулей в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="2bde1-109">Calls the [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method of the remaining plug-ins in that collection.</span></span>
4.  <span data-ttu-id="2bde1-110">Если подключаемый модуль, вызвавший исключение, является синхронным подключаемым модулем, то объект [ErrorData](/previous-versions/ms575221(v=vs.100)) (в управляемом коде) добавляется в очередь вывода.</span><span class="sxs-lookup"><span data-stu-id="2bde1-110">If the plug-in that threw the exception is a synchronous plug-in, the [ErrorData](/previous-versions/ms575221(v=vs.100)) object (in managed code) is added to the output queue.</span></span>
5.  <span data-ttu-id="2bde1-111">Объект [**RealTimeStylus**](realtimestylus-class.md) возобновляет нормальную обработку исходных данных.</span><span class="sxs-lookup"><span data-stu-id="2bde1-111">The [**RealTimeStylus**](realtimestylus-class.md) object resumes normal processing of the original data.</span></span>

<span data-ttu-id="2bde1-112">Если подключаемый модуль создает исключение из метода [**ошибки**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , объект [**RealTimeStylus**](realtimestylus-class.md) перехватывает исключение, но не создает новый объект [ErrorData](/previous-versions/ms575221(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="2bde1-112">If a plug-in throws an exception from its [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) method, the [**RealTimeStylus**](realtimestylus-class.md) object catches the exception but does not generate a new [ErrorData](/previous-versions/ms575221(v=vs.100)) object.</span></span> <span data-ttu-id="2bde1-113">Дополнительные сведения о добавлении ErrorData в очередь см. в разделе [подключаемые данные и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="2bde1-113">For more information about how ErrorData is added to the queue, see [Plug-in Data and the RealTimeStylus Class](plug-in-data-and-the-realtimestylus-class.md).</span></span>

<span data-ttu-id="2bde1-114">Объект [**RealTimeStylus**](realtimestylus-class.md) не останавливает обработку данных из потока данных пера планшета, когда один из подключаемых модулей создает исключение.</span><span class="sxs-lookup"><span data-stu-id="2bde1-114">The [**RealTimeStylus**](realtimestylus-class.md) object does not stop processing data from the tablet pen's data stream when one of its plug-ins throws an exception.</span></span> <span data-ttu-id="2bde1-115">В зависимости от проекта некоторые подключаемые модули могут подписываться на уведомления [ErrorData](/previous-versions/ms575221(v=vs.100)) и изменять их поведение при возникновении исключения.</span><span class="sxs-lookup"><span data-stu-id="2bde1-115">Depending on your design, some of your plug-ins may need to subscribe to the [ErrorData](/previous-versions/ms575221(v=vs.100)) notification and modify their behavior when an exception occurs.</span></span>

 

 
