---
description: Описывает структуры, используемые интерфейсами видео Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Видеоструктуры Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692050"
---
# <a name="direct3d-9-video-structures"></a>Видеоструктуры Direct3D 9

Описывает структуры, используемые интерфейсами видео Microsoft Direct3D 9.



| Структура                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D \_ ОМАК**](d3d-omac.md)<br/> Содержит код проверки подлинности сообщения (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAESный \_ \_ вектор IV**](d3daes-ctr-iv.md)<br/> Содержит вектор инициализации (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ Настройка \_ входных данных**](d3dauthenticatedchannel-configure-input.md)<br/> Содержит входные данные для метода [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ настроить \_ выходные данные**](d3dauthenticatedchannel-configure-output.md)<br/> Содержит ответ на вызов метода [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ конфигуреинитиализе**](d3dauthenticatedchannel-configureinitialize.md)<br/> Содержит входные данные для команды [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ конфигурепротектион**](d3dauthenticatedchannel-configureprotection.md)<br/> Содержит входные данные для [**команды \_ защиты D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ конфигурекриптосессион**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Содержит входные данные для [**команды \_ CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-cryptosession.md) .<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ конфигурешаредресаурце**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Содержит входные данные для [**команды \_ шаредресаурце D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-sharedresource.md) .<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ конфигуреункомпресседенкриптион**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Содержит входные данные для [**команды \_ енкриптионвхенакцессибле D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .<br/>                                                                   |
| [**\_ \_ Флаги защиты D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md)<br/> Задает уровень защиты содержимого видео.<br/>                                                                                                                                                                                                   |
| [**\_ \_ Входные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md)<br/> Содержит входные данные для метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                                     |
| [**\_ \_ Выходные данные запроса D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md)<br/> Содержит ответ на вызов метода [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                        |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеричаннелтипе**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ чаннелтипе**](d3dauthenticatedquery-channeltype.md) .<br/>                                                                                                                     |
| [**\_ \_ Входные данные куерикриптосессион D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                                |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерикриптосессион**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                             |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеридевицехандле**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ девицехандле**](d3dauthenticatedquery-devicehandle.md) .<br/>                                                                                                                 |
| [**\_ \_ Входные данные куеревиктионенкриптионгуид D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                                |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуид**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуид**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                             |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеревиктионенкриптионгуидкаунт**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ енкриптионвхенакцессиблегуидкаунт**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .<br/>                                         |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куеринфобустипе**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ акцессибилитяттрибутес**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**\_ \_ Входные данные куерйоутпутид D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Содержит данные интпут для запроса [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                   |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутид**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутид**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                 |
| [**\_ \_ Входные данные куерйоутпутидкаунт D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                                |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерйоутпутидкаунт**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ аутпутидкаунт**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                             |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерипротектион**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Содержит ответ на запрос [**\_ защиты D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .<br/>                                                                                                                         |
| [**\_ \_ Входные данные куерирестриктедшаредресаурцепроцесс D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Содержит входные данные для запроса [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                        |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесс**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесс**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                     |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерирестриктедшаредресаурцепроцесскаунт**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ рестриктедшаредресаурцепроцесскаунт**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .<br/>                 |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнкомпресседенкриптионлевел**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ куррентенкриптионвхенакцессибле**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .<br/>                                             |
| [**\_ \_ Выходные данные D3DAUTHENTICATEDCHANNEL куерюнрестриктедпротектедшаредресаурцекаунт**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Содержит ответ на запрос [**D3DAUTHENTICATEDQUERY \_ унрестриктедпротектедшаредресаурцекаунт**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Описание возможностей защиты содержимого драйвера дисплея.<br/>                                                                                                                                                                                                                    |
| [**\_Сведения о блоке D3DENCRYPTED \_**](d3dencrypted-block-info.md)<br/> Указывает, какие байты зашифрованы в защищенной видеоповерхности.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Указывает возможности наложения оборудования для устройства Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**дксвабуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Задает буфер для метода [**IDirect3DDXVADevice9:: Execute**](idirect3ddxvadevice9-execute.md) .<br/>                                                                                                                                                                                                  |
| [**дксвакомпбуфферинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Указывает требования для сжатых поверхностей для ускорения видео DirectX (ДКСВА).<br/>                                                                                                                                                                                                         |
| [**дксваункомпдатаинфо**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Задает размеры и формат пикселей для несжатых поверхностей для декодирования видео ДКСВА.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[API-интерфейсы видео Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




