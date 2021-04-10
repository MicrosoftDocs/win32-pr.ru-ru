---
title: Контроллеры домена и функции управления репликацией
description: Этот раздел содержит список функций, используемых для контроллера домена и управления репликацией.
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069791"
---
# <a name="domain-controller-and-replication-management-functions"></a>Контроллеры домена и функции управления репликацией

Контроллеры домена и функции управления репликацией предоставляют средства для поиска данных о контроллере домена, преобразования имен сетевых объектов между различными форматами, управления именами участников-служб (SPN) и агентами службы каталогов (DSA) и управления репликацией серверов. Следующие функции позволяют разработчикам работать с контроллерами домена, репликацией и службой каталогов.

-   [**дсаддсидхистори**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**дсбинд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**дсбиндингсеттимеаут**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**дсбиндтоистг**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**дсбиндвискред**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**дсбиндвисспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**дсбиндвисспнекс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**дсклиентмакеспнфортаржетсервер**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**дскраккспн**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**дскраккункуотедмангледрдн**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**дсфридомаинконтроллеринфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**дсфринамересулт**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**дсфрипассвордкредентиалс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**дсфрисчемагуидмап**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**дсфриспнаррай**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**дсжетдомаинконтроллеринфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**дсжетрднв**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**дсинхеритсекуритидентити**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**дсисмангледдн**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**дсисмангледрднвалуе**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**дслистдомаинсинсите**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**дслистинфофорсервер**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**дслистролес**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**дслистсерверсфордомаининсите**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**дслистсерверсинсите**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**дслистситес**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**дсмакепассвордкредентиалс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**дсмакеспн**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**дсмапсчемагуидс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**дскуериситесбикост**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**дскуериситесфри**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**дскуотерднвалуе**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**дсремоведсдомаин**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**дсремоведссервер**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**дсрепликаадд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**дсрепликаконсистенцичекк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**дсрепликадел**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**дсрепликафриинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**дсрепликажетинфо**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**дсрепликамодифи**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**дсрепликасинкалл**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**дсрепликаупдатерефс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**дсрепликаверифйобжектс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**дссерверрегистерспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**дсунбинд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**дсункуотерднвалуе**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**дсвритеаккаунтспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**синкупдатепрок**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

Для большинства из этих функций необходим маркер, привязанный к службе каталогов. Функции [**дсбинд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda) и [**дсбиндвискред**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda) запускают сеанс RPC с определенным контроллером домена, а затем привязывают маркер к службе каталогов и возвращают этот обработчик. Если этот маркер больше не требуется, используйте функцию [**дсунбинд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) , чтобы завершить сеанс RPC и отменить привязку этого маркера.

Репликация выполняется между исходным сервером и целевым сервером. Сервер-источник содержит список целевых серверов, на которые он должен выполнять репликацию, а целевой сервер поддерживает список исходных серверов, с которых он получает репликацию. Используйте функцию [**дсрепликаадд**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) для добавления в список исходных серверов на целевом сервере и используйте функцию [**дсрепликадел**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) для удаления ссылок из списка исходных серверов на целевом сервере. Функцию [**дсрепликамодифи**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya) можно использовать для изменения существующей ссылки на исходный сервер на целевом сервере. Чтобы изменить список целевых серверов на исходном сервере, используйте функцию [**дсрепликаупдатерефс**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) .

Фактическая репликация выполняется функциями [**дсрепликасинк**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) и [**дсрепликасинкалл**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) . Функция **дсрепликасинк** синхронизирует конкретный целевой сервер с одним исходным сервером. Используйте функцию **дсрепликасинкалл** для синхронизации целевого сервера со всеми остальными серверами сайта.

 

 