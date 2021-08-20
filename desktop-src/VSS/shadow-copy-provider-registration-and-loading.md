---
description: Регистрация и загрузка поставщика теневого копирования
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Регистрация и загрузка поставщика теневого копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998114"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Регистрация и загрузка поставщика теневого копирования

## <a name="provider-registration"></a>Регистрация поставщика

Только поставщики вызовов VSS. Поставщик регистрируется для вызовов, вызывая [**ивссадмин:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), передавая **\_ \_ оборудование VSS Prov** для параметра *епровидертипе* . После регистрации поставщик будет задействован в управлении теневыми копиями до отмены регистрации с помощью [**ивссадмин:: унрегистерпровидер**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Загрузка и выгрузка поставщика

Поставщики можно часто загружать и выгружать. Поставщики могут реализовывать [**ивсспровидернотификатионс**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) , чтобы определить, когда служба VSS загружает или выгружает поставщик.

 

 



