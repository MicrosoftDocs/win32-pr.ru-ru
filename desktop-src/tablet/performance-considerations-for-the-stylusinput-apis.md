---
description: Описание способов повышения производительности при использовании интерфейсов прикладного программирования (API) Стилусинпут.
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Рекомендации по производительности для API Стилусинпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818097"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="6d03b-103">Рекомендации по производительности для API Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="6d03b-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="6d03b-104">В следующем списке описаны некоторые способы повышения производительности приложений, использующих API-интерфейсы Стилусинпут.</span><span class="sxs-lookup"><span data-stu-id="6d03b-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="6d03b-105">Используйте свойство [Microsoft. стилусинпут. истилуссинкплугин. увлечений](/previous-versions/ms824752(v=msdn.10)) или [Microsoft. стилусинпут. истилусасинкплугин.](/previous-versions/ms824769(v=msdn.10)) , чтобы подписываться только на данные, относящиеся к подключаемому модулю.</span><span class="sxs-lookup"><span data-stu-id="6d03b-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="6d03b-106">Это сокращает общее число вызовов методов, которые создает объект [**RealTimeStylus**](realtimestylus-class.md) , и сокращает сложность подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="6d03b-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="6d03b-107">Объект **RealTimeStylus** проверяет свойство DataObject только при присоединении подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="6d03b-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="6d03b-108">Сократите сложность синхронных подключаемых модулей. Синхронные подключаемые модули, как правило, вызываются потоком объекта [**RealTimeStylus**](realtimestylus-class.md) и могут вносить задержки в сбор рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="6d03b-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="6d03b-109">Попробуйте сделать подключаемый модуль асинхронным.</span><span class="sxs-lookup"><span data-stu-id="6d03b-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="6d03b-110">Если подключаемый модуль является сложным и ему нужно добавить пользовательские данные в очередь объекта [**RealTimeStylus**](realtimestylus-class.md) , рассмотрите возможность использования каскадной модели **RealTimeStylus** и добавления подключаемого модуля в синхронную коллекцию подключаемых модулей объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="6d03b-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="6d03b-111">Дополнительные сведения о каскадной модели **RealTimeStylus** см. в статье [каскадная модель RealTimeStylus](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="6d03b-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 
