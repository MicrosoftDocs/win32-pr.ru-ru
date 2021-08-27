---
description: Функция Сетупсетсаурцелист будет открывать или создавать исходный список в системе пользователей.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Использование списка источников MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada1fa55a1c0defea2f344200eb331b8031dedfa66336510fb55b6fb77213a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100634"
---
# <a name="using-the-mru-source-list"></a>Использование списка источников MRU

Функция [**сетупсетсаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) будет открывать или создавать исходный список в системе пользователя. Можно задать список пользователей, системный список, сочетание списков пользователей и систем, а также временный список источников MRU. Если используется временный список, он будет единственным списком, доступным для приложения установки до тех пор, пока не будет вызван [**сетупканцелтемпорарисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) , или **сетупсетсаурцелист** будет вызван второй раз.

После задания списка можно запросить исходный список с помощью [**сетупкуерисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) , чтобы получить массив исходных путей. Если массив исходного списка больше не нужен, необходимо вызвать функцию [**сетупфрисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) , чтобы освободить ресурсы, выделенные [**сетупкуерисаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).

Чтобы добавить путь к исходному списку, который находится в системе пользователя или во временном списке, вызовите [**сетупаддтосаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista). Если указанный исходный список не является временным, он остается в системе пользователя и доступен для последующих установок.

Чтобы удалить путь из исходного пути, вызовите функцию [**сетупремовефромсаурцелист**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .

 

 



