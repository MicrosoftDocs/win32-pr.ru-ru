---
title: Перечисление DownloadMode (Deliveryoptimization. h)
description: Определяет различные режимы загрузки, используемые оптимизацией доставки.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Использование BITS в обход оптимизации доставки. Используйте этот режим, например, чтобы клиенты могли использовать BranchCache. перечисление
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543728"
---
# <a name="downloadmode-enumeration"></a>Перечисление DownloadMode

Определяет различные режимы загрузки, используемые оптимизацией доставки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Этот параметр отключает одноранговый кэш, но по-прежнему позволяет оптимизировать доставку для загрузки содержимого с серверов Майкрософт. Этот режим использует дополнительные метаданные, предоставляемые облачными службами оптимизации доставки, для надежного и эффективного скачивания без одноранговых устройств.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Это стандартный рабочий режим оптимизации доставки, обеспечивающий одноранговый обмен данными в пределах одной сети.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

если задан режим группы, группа выбирается автоматически на основе сайта домен Active Directory служб (AD DS) (Windows 10, версия 1607) или домена, на который проверяется подлинность устройства (Windows 10, версия 1511). В групповом режиме пиринг осуществляется по внутренним подсетям между устройствами, принадлежащим к одной и той же группе, включая устройства в удаленных офисах. Вы можете использовать параметр GroupID для создания собственной пользовательской группы независимо от доменов и сайтов AD DS. Режим групповой загрузки рекомендуется для большинства организаций, которые заинтересованы в оптимизации пропускной способности при оптимизации доставки.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Включение одноранговых интернет-источников для оптимизации доставки.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

Простой режим полностью отключает использование облачных служб оптимизации доставки (для автономных сред). Оптимизация доставки автоматически переходит в этот режим, если облачные службы оптимизации доставки недоступны, недостижимы или когда размер файла содержимого меньше 10 МБ. В этом режиме оптимизация доставки обеспечивает надежное скачивание без для однорангового кэширования.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

Использование BITS в обход оптимизации доставки. Используйте этот режим, например, чтобы клиенты могли использовать BranchCache.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------|----------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>      |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>  |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
