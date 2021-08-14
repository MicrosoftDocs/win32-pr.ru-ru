---
title: Интерфейс Итссбтаржетекс
description: Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, описание
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fb9be0e4cf5c0395efa93d308fdfa45362a7ac8919ab49a108700106aff6081b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989824"
---
# <a name="itssbtargetex-interface"></a>Интерфейс Итссбтаржетекс

Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.

этот интерфейс доступен только в Windows Server 2012 R2 с установленным [KB3091411](https://support.microsoft.com/kb/3091411) . Свойство [**таржетлоад**](itssbtarget-targetload.md) интерфейса [**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) доступно начиная с Windows Server 2016.

## <a name="members"></a>Элементы

Интерфейс **итссбтаржетекс** наследует от [**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget). **Итссбтаржетекс** также имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Интерфейс **итссбтаржетекс** имеет следующие свойства.



| Свойство                                                                      | Тип доступа           | Описание                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Чтение/запись<br/> | Возвращает или задает имя среды, связанной с целевым объектом.<br/> |
| [**фармнаме**](itssbtarget-farmname.md)<br/>                           | Чтение/запись<br/> | Указывает или получает имя фермы, к которой присоединен этот целевой объект.<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | Чтение/запись<br/> | Возвращает или задает внешние IP-адреса целевого объекта.<br/>                |
| [**нумпендингконнектионс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Только для чтения<br/>  | Возвращает число ожидающих пользовательских соединений для целевого объекта.<br/>               |
| [**нумсессионс**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Только для чтения<br/>  | Возвращает число сеансов, обслуживаемых брокером для целевого объекта.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Чтение/запись<br/> | Указывает или получает полное доменное имя целевого объекта.<br/>          |
| [**таржетлоад**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Только для чтения<br/>  | Извлекает относительную нагрузку на целевой объект.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Чтение/запись<br/> | Указывает или получает имя целевого объекта.<br/>                                 |
| [**таржетнетбиос**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Чтение/запись<br/> | Указывает или получает NetBIOS-имя целевого объекта.<br/>                         |
| [**таржетпропертисет**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Чтение/запись<br/> | Указывает или получает набор свойств для целевого объекта.<br/>                        |
| [**таржетстате**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Чтение/запись<br/> | Указывает или получает целевое состояние.<br/>                                       |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                |
| Поддержка конца сервера<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ итссбтаржетекс определен как 74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Интерфейсы виртуализации удаленный рабочий стол](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

