```c
struct ether_addr 
{
    uint8_t addr_bytes[6]; /**< Address bytes in transmission order */
};

struct ether_hdr 
{
    struct ether_addr d_addr; /**< Destination address. */
    struct ether_addr s_addr; /**< Source address. */
    uint16_t ether_type;      /**< Frame type. */
};

struct vlan_hdr
{
    uint16_t vlan_tci;
    uint16_t eth_proto;
};

struct ipv4_hdr 
{
    uint8_t  version_ihl;       /**< version and header length */
    uint8_t  type_of_service;   /**< type of service */
    uint16_t total_length;      /**< length of packet */
    uint16_t packet_id;         /**< packet ID */
    uint16_t fragment_offset;   /**< fragmentation offset */
    uint8_t  time_to_live;      /**< time to live */
    uint8_t  next_proto_id;     /**< protocol ID */
    uint16_t hdr_checksum;      /**< header checksum */
    uint32_t src_addr;          /**< source address */
    uint32_t dst_addr;          /**< destination address */
};

struct ipv6_hdr 
{
    uint32_t vtc_flow;     /**< IP version, traffic class & flow label. */
    uint16_t payload_len;  /**< IP packet length - includes sizeof(ip_header). */
    uint8_t  proto;        /**< Protocol, next header. */
    uint8_t  hop_limits;   /**< Hop limits. */
    uint8_t  src_addr[16]; /**< IP address of source host. */
    uint8_t  dst_addr[16]; /**< IP address of destination host(s). */
};

struct tcp_hdr 
{
    uint16_t src_port;  /**< TCP source port. */
    uint16_t dst_port;  /**< TCP destination port. */
    uint32_t sent_seq;  /**< TX data sequence number. */
    uint32_t recv_ack;  /**< RX data acknowledgement sequence number. */
    uint8_t  data_off;  /**< Data offset. */
    uint8_t  tcp_flags; /**< TCP flags */
    uint16_t rx_win;    /**< RX flow control window. */
    uint16_t cksum;     /**< TCP checksum. */
    uint16_t tcp_urp;   /**< TCP urgent pointer, if any. */
};

struct udp_hdr 
{
    uint16_t src_port;    /**< UDP source port. */
    uint16_t dst_port;    /**< UDP destination port. */
    uint16_t dgram_len;   /**< UDP datagram length */
    uint16_t dgram_cksum; /**< UDP datagram checksum */
};

```
