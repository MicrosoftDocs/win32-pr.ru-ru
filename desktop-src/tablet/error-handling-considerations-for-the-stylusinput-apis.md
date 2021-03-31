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
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Рекомендации по обработке ошибок для API Стилусинпут

Необработанные исключения, вызванные подключаемым модулем, перехватываются объектом [**RealTimeStylus**](realtimestylus-class.md) . Когда подключаемый модуль создает исключение, нормальный поток данных прерывается. Объект **RealTimeStylus** :

1.  Создает объект [ErrorData](/previous-versions/ms575221(v=vs.100)) (в управляемом коде).
2.  Вызывает метод [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (в управляемом коде — метод [Microsoft. стилусинпут. истилуссинкплугин. Error](/previous-versions/ms824754(v=msdn.10)) или [Microsoft. стилусинпут. истилусасинкплугин. Error](/previous-versions/ms824771(v=msdn.10)) ) подключаемого модуля, который вызвал исключение.
3.  Вызывает метод [**Error**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) для оставшихся подключаемых модулей в этой коллекции.
4.  Если подключаемый модуль, вызвавший исключение, является синхронным подключаемым модулем, то объект [ErrorData](/previous-versions/ms575221(v=vs.100)) (в управляемом коде) добавляется в очередь вывода.
5.  Объект [**RealTimeStylus**](realtimestylus-class.md) возобновляет нормальную обработку исходных данных.

Если подключаемый модуль создает исключение из метода [**ошибки**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , объект [**RealTimeStylus**](realtimestylus-class.md) перехватывает исключение, но не создает новый объект [ErrorData](/previous-versions/ms575221(v=vs.100)) . Дополнительные сведения о добавлении ErrorData в очередь см. в разделе [подключаемые данные и класс RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

Объект [**RealTimeStylus**](realtimestylus-class.md) не останавливает обработку данных из потока данных пера планшета, когда один из подключаемых модулей создает исключение. В зависимости от проекта некоторые подключаемые модули могут подписываться на уведомления [ErrorData](/previous-versions/ms575221(v=vs.100)) и изменять их поведение при возникновении исключения.

 

 
