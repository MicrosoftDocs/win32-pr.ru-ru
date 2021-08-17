---
description: устанавливает зарегистрированный сертификат из файла личных данных Exchange (PFX) в хранилище сертификатов.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: инсталлреспонсефромпфкс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540e719f098d227afac4af59fd2d296d9d06606d04b9de80cf1e24081918d6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117777610"
---
# <a name="installresponsefrompfx"></a>инсталлреспонсефромпфкс

пример инсталлреспонсефромпфкс устанавливает зарегистрированный сертификат из файла личных данных Exchange (PFX) в хранилище сертификатов.

## <a name="location"></a>Расположение

при установке пакета microsoft Windows Software Development Kit (SDK) образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security ssl \\ Certificate \\ \\ инсталлреспонсефромпфкс.

## <a name="discussion"></a>Разговор

Пример Инсталлреспонсефромпфкс:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать:
    -   Имя образца.
    -   Имя PFX-файла, содержащего зарегистрированный сертификат.
    -   Пароль, связанный с PFX-файлом.
2.  Считывает PFX-файл, сначала пытается выполнить формат Base64, а двоичный формат — в случае сбоя Base64. Функция Декодефилев () определена в Енроллкоммон. cpp.
3.  Преобразует зарегистрированный сертификат в **BSTR** и использует его для инициализации объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . Функция Конвертвсзтобстр определена в Енроллкоммон. cpp.
4.  Устанавливает сертификат в хранилище сертификатов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[енроллеобокмк](enrolleobocmc.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 



