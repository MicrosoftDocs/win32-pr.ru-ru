---
description: В \_ константах фонефеатуре перечислены операции, которые могут быть вызваны на телефоне с помощью этого API. Каждое из значений ФОНЕФЕАТУРЕ \_ (за исключением фонефеатуре \_ женерикфоне) соответствует функции TAPI с идентичным или похожим именем.
ms.assetid: 361b3080-3650-48a2-a1b7-f05d72777f9a
title: Константы PHONEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e0333135df4185348f3471aa4184a0cd93e907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689532"
---
# <a name="phonefeature_-constants"></a>\_Константы фонефеатуре

В константах **фонефеатуре \_** перечислены операции, которые могут быть вызваны на телефоне с помощью этого API. Каждое из значений ФОНЕФЕАТУРЕ \_ (за исключением фонефеатуре \_ женерикфоне) соответствует функции TAPI с идентичным или похожим именем.



| Константа/значение                                                                                                                                                                                                                                                                            | Описание                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PHONEFEATURE_GETBUTTONINFO"></span><span id="phonefeature_getbuttoninfo"></span><dl> <dt>**Фонефеатуре \_ ЖЕТБУТТОНИНФО**</dt> <dt>0x00000001</dt> </dl>                      | [**фонежетбуттонинфо**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_GETDATA"></span><span id="phonefeature_getdata"></span><dl> <dt>**Фонефеатуре \_ GETDATA**</dt> <dt>0x00000002</dt> </dl>                                        | [**фонежетдата**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata)<br/>                                         |
| <span id="PHONEFEATURE_GETDISPLAY"></span><span id="phonefeature_getdisplay"></span><dl> <dt>**Фонефеатуре \_ @ ЭКРАН**</dt> <dt>0x00000004</dt> </dl>                               | [**фонежетдисплай**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_GETGAINHANDSET"></span><span id="phonefeature_getgainhandset"></span><dl> <dt>**Фонефеатуре \_ ЖЕТГАИНХАНДСЕТ**</dt> <dt>0x00000008</dt> </dl>                   | [**фонежетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/>             |
| <span id="PHONEFEATURE_GETGAINSPEAKER"></span><span id="phonefeature_getgainspeaker"></span><dl> <dt>**Фонефеатуре \_ ЖЕТГАИНСПЕАКЕР**</dt> <dt>0x00000010</dt> </dl>                   | [**фонежетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) ФОНЕХУКСВИТЧДЕВ \_ докладчик<br/>             |
| <span id="PHONEFEATURE_GETGAINHEADSET"></span><span id="phonefeature_getgainheadset"></span><dl> <dt>**Фонефеатуре \_ ЖЕТГАИНХЕАДСЕТ**</dt> <dt>0x00000020</dt> </dl>                   | [**фонежетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonegetgain) ФОНЕХУКСВИТЧДЕВ \_ гарнитура<br/>             |
| <span id="PHONEFEATURE_GETHOOKSWITCHHANDSET"></span><span id="phonefeature_gethookswitchhandset"></span><dl> <dt>**Фонефеатуре \_ ЖЕСУКСВИТЧХАНДСЕТ**</dt> <dt>0x00000040</dt> </dl> | [**фонежесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHSPEAKER"></span><span id="phonefeature_gethookswitchspeaker"></span><dl> <dt>**Фонефеатуре \_ ЖЕСУКСВИТЧСПЕАКЕР**</dt> <dt>0x00000080</dt> </dl> | [**фонежесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/> |
| <span id="PHONEFEATURE_GETHOOKSWITCHHEADSET"></span><span id="phonefeature_gethookswitchheadset"></span><dl> <dt>**Фонефеатуре \_ ЖЕСУКСВИТЧХЕАДСЕТ**</dt> <dt>0x00000100</dt> </dl> | [**фонежесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/> |
| <span id="PHONEFEATURE_GETLAMP"></span><span id="phonefeature_getlamp"></span><dl> <dt>**Фонефеатуре \_ ЛАМПА**</dt> <dt>0x00000200</dt> </dl>                                        | [**фонежетламп**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp)<br/>                                         |
| <span id="PHONEFEATURE_GETRING"></span><span id="phonefeature_getring"></span><dl> <dt>**Фонефеатуре \_**</dt> <dt>0x00000400а</dt> "Звонок" </dl>                                        | [**фонежетринг**](/windows/desktop/api/Tapi/nf-tapi-phonegetring)<br/>                                         |
| <span id="PHONEFEATURE_GETVOLUMEHANDSET"></span><span id="phonefeature_getvolumehandset"></span><dl> <dt>**Фонефеатуре \_ ЖЕТВОЛУМЕХАНДСЕТ**</dt> <dt>0x00000800</dt> </dl>             | [**фонежетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/>         |
| <span id="PHONEFEATURE_GETVOLUMESPEAKER"></span><span id="phonefeature_getvolumespeaker"></span><dl> <dt>**Фонефеатуре \_ ЖЕТВОЛУМЕСПЕАКЕР**</dt> <dt>0x00001000</dt> </dl>             | [**фонежетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) ФОНЕХУКСВИТЧДЕВ \_ докладчик<br/>         |
| <span id="PHONEFEATURE_GETVOLUMEHEADSET"></span><span id="phonefeature_getvolumeheadset"></span><dl> <dt>**Фонефеатуре \_ ЖЕТВОЛУМЕХЕАДСЕТ**</dt> <dt>0x00002000</dt> </dl>             | [**фонежетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonegetvolume) ФОНЕХУКСВИТЧДЕВ \_ гарнитура<br/>         |
| <span id="PHONEFEATURE_SETBUTTONINFO"></span><span id="phonefeature_setbuttoninfo"></span><dl> <dt>**Фонефеатуре \_ СЕТБУТТОНИНФО**</dt> <dt>0x00004000</dt> </dl>                      | [**фонесетбуттонинфо**](/windows/desktop/api/Tapi/nf-tapi-phonesetbuttoninfo)<br/>                             |
| <span id="PHONEFEATURE_SETDATA"></span><span id="phonefeature_setdata"></span><dl> <dt>**Фонефеатуре \_ SETDATA**</dt> <dt>0x00008000</dt> </dl>                                        | [**фонесетдата**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata)<br/>                                         |
| <span id="PHONEFEATURE_SETDISPLAY"></span><span id="phonefeature_setdisplay"></span><dl> <dt>**Фонефеатуре \_ СЕТДИСПЛАЙ**</dt> <dt>0x00010000</dt> </dl>                               | [**фонесетдисплай**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay)<br/>                                   |
| <span id="PHONEFEATURE_SETGAINHANDSET"></span><span id="phonefeature_setgainhandset"></span><dl> <dt>**Фонефеатуре \_ СЕТГАИНХАНДСЕТ**</dt> <dt>0x00020000</dt> </dl>                   | [**фонесетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/>             |
| <span id="PHONEFEATURE_SETGAINSPEAKER"></span><span id="phonefeature_setgainspeaker"></span><dl> <dt>**Фонефеатуре \_ СЕТГАИНСПЕАКЕР**</dt> <dt>0x00040000</dt> </dl>                   | [**фонесетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) ФОНЕХУКСВИТЧДЕВ \_ докладчик<br/>             |
| <span id="PHONEFEATURE_SETGAINHEADSET"></span><span id="phonefeature_setgainheadset"></span><dl> <dt>**Фонефеатуре \_ СЕТГАИНХЕАДСЕТ**</dt> <dt>0x00080000</dt> </dl>                   | [**фонесетгаин**](/windows/desktop/api/Tapi/nf-tapi-phonesetgain) ФОНЕХУКСВИТЧДЕВ \_ гарнитура<br/>             |
| <span id="PHONEFEATURE_SETHOOKSWITCHHANDSET"></span><span id="phonefeature_sethookswitchhandset"></span><dl> <dt>**Фонефеатуре \_ СЕСУКСВИТЧХАНДСЕТ**</dt> <dt>0x00100000</dt> </dl> | [**фонесесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHSPEAKER"></span><span id="phonefeature_sethookswitchspeaker"></span><dl> <dt>**Фонефеатуре \_ СЕСУКСВИТЧСПЕАКЕР**</dt> <dt>0x00200000</dt> </dl> | [**фонесесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) ФОНЕХУКСВИТЧДЕВ \_ докладчик<br/> |
| <span id="PHONEFEATURE_SETHOOKSWITCHHEADSET"></span><span id="phonefeature_sethookswitchheadset"></span><dl> <dt>**Фонефеатуре \_ СЕСУКСВИТЧХЕАДСЕТ**</dt> <dt>0x00400000</dt> </dl> | [**фонесесуксвитч**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) ФОНЕХУКСВИТЧДЕВ \_ гарнитура<br/> |
| <span id="PHONEFEATURE_SETLAMP"></span><span id="phonefeature_setlamp"></span><dl> <dt>**Фонефеатуре \_ СЕТЛАМП**</dt> <dt>0x00800000</dt> </dl>                                        | [**фонесетламп**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp)<br/>                                         |
| <span id="PHONEFEATURE_SETRING"></span><span id="phonefeature_setring"></span><dl> <dt>**Фонефеатуре \_ СЕТРИНГ**</dt> <dt>0x01000000</dt> </dl>                                        | [**фонесетринг**](/windows/desktop/api/Tapi/nf-tapi-phonesetring)<br/>                                         |
| <span id="PHONEFEATURE_SETVOLUMEHANDSET"></span><span id="phonefeature_setvolumehandset"></span><dl> <dt>**Фонефеатуре \_ СЕТВОЛУМЕХАНДСЕТ**</dt> <dt>0x02000000</dt> </dl>             | [**фонесетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) ФОНЕХУКСВИТЧДЕВная \_ трубка<br/>         |
| <span id="PHONEFEATURE_SETVOLUMESPEAKER"></span><span id="phonefeature_setvolumespeaker"></span><dl> <dt>**Фонефеатуре \_ СЕТВОЛУМЕСПЕАКЕР**</dt> <dt>0x04000000</dt> </dl>             | [**фонесетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) ФОНЕХУКСВИТЧДЕВ \_ докладчик<br/>         |
| <span id="PHONEFEATURE_SETVOLUMEHEADSET"></span><span id="phonefeature_setvolumeheadset"></span><dl> <dt>**Фонефеатуре \_ СЕТВОЛУМЕХЕАДСЕТ**</dt> <dt>0x08000000</dt> </dl>             | [**фонесетволуме**](/windows/desktop/api/Tapi/nf-tapi-phonesetvolume) ФОНЕХУКСВИТЧДЕВ \_ гарнитура<br/>         |
| <span id="PHONEFEATURE_GENERICPHONE"></span><span id="phonefeature_genericphone"></span><dl> <dt>**Фонефеатуре \_ ЖЕНЕРИКФОНЕ**</dt> <dt>0x10000000</dt> </dl>                         | (относится только к приложениям, использующим TAPI 3,0 и более поздние версии)<br/>                     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




