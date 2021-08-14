---
description: Как можно использовать функции резервного копирования служб сертификатов для резервного копирования базы данных служб сертификатов и связанных с ней файлов.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Резервное копирование служб сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773090"
---
# <a name="backing-up-certificate-services"></a>Резервное копирование служб сертификатов

Ниже приведен сценарий, показывающий, как можно использовать функции резервного копирования служб сертификатов для резервного копирования базы данных служб сертификатов и связанных с ней файлов.

1.  Загрузка библиотеки Certadm.dll в память (путем вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Извлеките адрес каждой из необходимых функций в Certadm.dll (с помощью [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Используйте эти адреса при вызове функций на оставшихся этапах.
3.  Вызовите [**цертсрвиссерверонлине**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) , чтобы определить, находятся ли службы сертификатов в сети. Для успешного выполнения операций резервного копирования службы сертификатов должны находиться в оперативном режиме.
4.  Вызовите [**цертсрвбаккуппрепаре**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) для запуска сеанса резервного копирования. Результирующий маркер контекста резервного копирования служб сертификации будет использоваться многими другими функциями резервного копирования.
5.  Вызовите [**цертсрвресторежетдатабаселокатионс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) , чтобы определить карту восстановления. На карте восстановления содержатся пути, используемые при восстановлении резервной копии. Сохраните информацию, полученную с помощью **цертсрвресторежетдатабаселокатионс** , в отдельном расположении приложения.
6.  Вызовите [**цертсрвбаккупжетдатабасенамес**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) , чтобы определить имена файлов базы данных для резервного копирования. Для каждого из этих файлов выполните шаги 7 – 9.
7.  Вызовите [**цертсрвбаккупопенфиле**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) , чтобы открыть файл для резервного копирования.
8.  Вызовите [**цертсрвбаккупреад**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) , чтобы прочитать часть байтов из файла, а затем вызовите подпрограммы для конкретного приложения, чтобы хранить байты на носителе резервной копии. Повторите этот шаг, пока не будут создаваться резервные копии всех байтов в файле.
9.  Вызовите [**цертсрвбаккупклосе**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) , чтобы закрыть файл.
10. Вызовите [**цертсрвбаккупжетбаккуплогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) , чтобы определить имена файлов журналов для резервного копирования. Для каждого из этих файлов выполните шаги 7 – 9.
11. Вызовите [**цертсрвбаккуптрункателогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) , чтобы усечь файлы журнала, которые были созданы в шагах 6 и 10. Этот шаг является необязательным. Однако вызывайте **цертсрвбаккуптрункателогс** только в том случае, если были созданы резервные копии всех файлов, возвращенных [**цертсрвбаккупжетдатабасенамес**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) и [**цертсрвбаккупжетбаккуплогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) (в противном случае операция восстановления завершится ошибкой). Дополнительные сведения см. на странице справочника по **цертсрвбаккуптрункателогс** .
12. Вызовите [**цертсрвбаккупжетдинамикфилелист**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) , чтобы определить имена файлов, не являющихся базами данных, для резервного копирования. Эти файлы идентифицируются только функцией и должны быть архивированы другими средствами.
13. Создайте резервную копию динамических файлов, указанных на шаге 12, с помощью подпрограмм, отделяющих от Certadm.dll.
14. Вызовите [**цертсрвбаккупенд**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) , чтобы завершить сеанс резервного копирования.
15. Вызовите [**цертсрвбаккупфри**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) по мере необходимости, чтобы освободить буферы, выделенные определенными функциями резервного копирования служб сертификатов. Вызовы [**цертсрвбаккупжетбаккуплогс**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw), [**цертсрвбаккупжетдатабасенамес**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)и [**цертсрвбаккупжетдинамикфилелист**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) будут выделять буферы, которые можно освободить путем вызова **CertSrvBackupFree**.
16. Освободите Certadm.dll ресурсы, вызвав [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary).

Сведения о привилегиях, необходимых для резервного копирования базы данных служб сертификатов и связанных файлов, см. [в разделе Установка привилегий резервного копирования и восстановления](setting-the-backup-and-restore-privileges.md).

 

 
