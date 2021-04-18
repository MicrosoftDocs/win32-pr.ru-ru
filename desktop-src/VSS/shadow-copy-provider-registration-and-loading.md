---
description: Регистрация и загрузка поставщика теневого копирования
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Регистрация и загрузка поставщика теневого копирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345002"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Регистрация и загрузка поставщика теневого копирования

## <a name="provider-registration"></a>Регистрация поставщика

Только поставщики вызовов VSS. Поставщик регистрируется для вызовов, вызывая [**ивссадмин:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), передавая **\_ \_ оборудование VSS Prov** для параметра *епровидертипе* . После регистрации поставщик будет задействован в управлении теневыми копиями до отмены регистрации с помощью [**ивссадмин:: унрегистерпровидер**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).

## <a name="provider-loading-and-unloading"></a>Загрузка и выгрузка поставщика

Поставщики можно часто загружать и выгружать. Поставщики могут реализовывать [**ивсспровидернотификатионс**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) , чтобы определить, когда служба VSS загружает или выгружает поставщик.

 

 



